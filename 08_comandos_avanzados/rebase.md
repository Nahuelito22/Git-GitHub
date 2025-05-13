# 🔄 `git rebase`

`git rebase` es un comando poderoso en Git utilizado para **aplicar los cambios de una rama sobre otra** de una manera más limpia que un merge. A diferencia de `git merge`, `rebase` reescribe el historial de tu rama y coloca tus commits encima de la rama base.

---

## 🧠 ¿Cuándo usar `rebase`?

- Cuando quieras mantener un historial de commits **más lineal**.
- Cuando quieras aplicar tus cambios sobre la rama principal (por ejemplo, `main` o `master`) y asegurarte de que tu rama esté **actualizada**.
- Para evitar el ruido de los merges en el historial de commits.

---

## 🛠️ Sintaxis básica

```bash
git rebase <rama-base>
```
Por ejemplo:
```bash
git rebase main
```
Esto mueve todos los commits de tu rama actual sobre la rama main.

---

## 📌 Pasos típicos
1. Estás trabajando en una rama llamada feature y querés actualizarla con los cambios de la rama main.
2. Primero, asegurate de tener todos los cambios de main:
```bash
git checkout main
git pull origin main
```
3. Luego, cambia a tu rama feature y haz el rebase:
```bash
git checkout feature
git rebase main
```
Esto coloca los commits de feature encima de los últimos cambios de main.

---

## ⚠️ Conflictos durante el rebase
Si hay conflictos durante el rebase, Git te pedirá que los resuelvas. Para resolverlos:
1. Solucioná los conflictos manualmente.
2. Marca los archivos resueltos:
```bash
git add <archivo-resuelto>
```
3.Continúa con el rebase:
```bash
git rebase --continue
```
Si te arrepentís en cualquier momento, podés abortar el rebase:
```bash
git rebase --abort
```

---


## ✅ Consejos útiles
* Usá git rebase solo en ramas locales antes de compartirlas con otros desarrolladores. No hagas rebase de ramas ya compartidas, ya que reescribe el historial y puede causar conflictos para otros colaboradores.
* Si necesitas rebase interactivo para cambiar el orden de los commits, eliminarlos o combinar varios, usá:
```bash
git rebase -i <commit-anterior>
```


---


## 🧪 Ejemplo práctico
Supongamos que tu rama feature se creó hace varios días y quieres asegurarte de que esté actualizada con la última versión de main:
```bash
git checkout feature
git fetch origin
git rebase origin/main
```
Esto actualizará tu rama feature con los cambios más recientes de main, manteniendo un historial limpio y lineal.

---

`git rebase` es una herramienta poderosa, pero requerís cuidado al usarla, ya que reescribe el historial de tu repositorio. Usa rebase para mantener un historial más limpio, pero evita usarlo en ramas compartidas para no causar problemas a tus compañeros de equipo.


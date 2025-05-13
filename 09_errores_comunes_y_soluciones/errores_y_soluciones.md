# 🧨 Errores Comunes y Cómo Solucionarlos en Git

Este archivo resume los errores más comunes que podés encontrar al trabajar con Git y cómo solucionarlos. Incluye conflictos, errores clásicos y formas de recuperar archivos eliminados o perdidos.

---

## ⚔️ 1. Conflictos de Merge

### ¿Qué es un conflicto?
Un conflicto ocurre cuando Git no puede fusionar dos ramas automáticamente porque los mismos archivos fueron modificados en ambas.

### Ejemplo típico:
Dos personas modifican la misma línea del mismo archivo en distintas ramas.

```bash
git merge rama-desarrollo
```
Resultado:
```bash
Auto-merging archivo.txt
CONFLICT (content): Merge conflict in archivo.txt
Automatic merge failed; fix conflicts and then commit the result.
```

#### Solución:
1. Git marcará el archivo en conflicto con líneas especiales:

```bash
txt
Copiar
Editar
<<<<<<< HEAD
Versión actual (rama donde estás)
=======
Versión de la rama que estás intentando fusionar
>>>>>>> rama-desarrollo
```

2. Editá el archivo manualmente, eligiendo qué versión conservar (o fusionando ambas).

3. Marcá el conflicto como resuelto:

```bash
git add archivo.txt
git commit
```

---


## 🚫 2. Errores Clásicos
a. "fatal: not a git repository"
Este error aparece cuando intentás usar Git en una carpeta que no es un repositorio.

##### Solución:
* Asegurate de estar dentro de una carpeta con .git.
* Si no es un repo, inicializalo:
```bash
git init
```

---

b. "Permission denied (publickey)"
Error típico al usar SSH sin tener la clave pública registrada en GitHub.

##### Solución:

1. Verificá si tenés una clave SSH:
```bash
ls ~/.ssh
```
2. Si no tenés, creala:
```bash
ssh-keygen -t rsa -b 4096 -C "tu-email@example.com"
```
3. Agregala a GitHub desde https://github.com/settings/keys

---


c. "You have not concluded your merge"
Intentaste hacer un merge pero no lo terminaste.

##### Solución:
```bash
git commit
```
O si querés cancelar el merge:
```bash
git merge --abort
```

---


d. "Updates were rejected because the remote contains work..."
Ocurre cuando el repositorio remoto tiene cambios que vos no tenés.

##### Solución:
```bash
git pull --rebase origin main
```
Luego podés pushear:
```bash
git push origin main
```

---

## 🔙 3. Recuperar Archivos
a. Deshacer cambios en un archivo no commiteado
```bash
git checkout -- archivo.txt
```
⚠️ Este comando elimina los cambios locales no guardados (no hay vuelta atrás).

---

b. Recuperar un archivo eliminado

Si el archivo fue eliminado pero no lo commiteaste aún:

```bash
git restore archivo.txt
```
Si ya lo habías commiteado:

```bash
git checkout HEAD^ archivo.txt
```
O usá:

```bash
git log -- archivo.txt
git checkout <commit-id> -- archivo.txt
```
---

c. Volver a un commit anterior
```bash
git checkout <commit-id>
```
Esto te lleva a un estado "detached HEAD". Si querés volver ahí como nueva rama:

```bash
git checkout -b nombre-rama
```

---

## ✅ Recomendaciones Finales
* Commiteá seguido para no perder trabajo.
* Usá ramas para experimentar, y no tocar main directamente.
* Ante la duda, hacé backup de tu carpeta antes de ejecutar comandos destructivos.

---

💡 Guardá esta guía. Cuando Git “se rompe”, puede salvarte el día. 😄

---
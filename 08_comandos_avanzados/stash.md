# 📦 `git stash`

El comando `git stash` es útil cuando estás trabajando en una rama y, de repente, necesitas cambiar de contexto (por ejemplo, ir a trabajar en otra rama), pero no quieres hacer un commit de los cambios incompletos que tienes. `git stash` guarda tus cambios locales para que puedas recuperarlos más tarde.

---

## 🧠 ¿Cuándo usar `git stash`?

- Cuando tienes cambios locales que aún no están listos para ser commitidos y necesitas cambiar de rama.
- Para guardar cambios temporalmente y evitar que interfieran con tu flujo de trabajo actual.
- Cuando quieras aplicar los cambios guardados en otro momento o en otra rama.

---

## 🛠️ Sintaxis básica

```bash
git stash
```
Este comando guarda todos los cambios sin comprometerlos. Después, puedes cambiar de rama y trabajar en otros cambios. Para volver a los cambios guardados, usás el comando git stash apply.

---

## 📌 Usos comunes
#### Guardar cambios

Si tienes cambios locales y necesitas guardarlos temporalmente, solo ejecuta:
```bash
git stash
```
Este comando guarda todos los cambios que no están comprometidos, y limpia tu área de trabajo (incluyendo archivos no seguidos).

#### Ver los stashes guardados
Para ver las entradas de tu stash, usa:
```bash
git stash list
```
Esto muestra una lista numerada de los stashes guardados.

#### Aplicar los cambios guardados
Para recuperar tus cambios guardados, ejecuta:
```bash
git stash apply
```

Esto aplica los cambios más recientes del stash a tu directorio de trabajo.

Si tienes múltiples stashes, puedes aplicar uno específico de la siguiente manera:
```bash
git stash apply stash@{n}
```
Donde n es el número del stash que deseas aplicar.

#### Eliminar un stash

Después de aplicar un stash, puedes eliminarlo de la lista con:

```bash
git stash drop stash@{n}
```

Si quieres eliminar todos los stashes, usa:
```bash
git stash clear
```

#### Guardar y cambiar de rama

Una de las características útiles de git stash es que puedes guardar tus cambios y cambiar de rama sin perder el trabajo no guardado.

1. Guarda tus cambios:
```bash 
git stash
```
2. Cambia de rama:
```bash 
git checkout <otra-rama>
```
3. Aplica los cambios guardados en la nueva rama:
```bash 
git stash apply
```

---


## ✅ Consejos útiles
* Si querés guardar solo ciertos archivos, puedes usar la opción -p para seleccionar interactivamente qué cambios guardar:
```bash 
git stash -p
```

* `git stash` también guarda cambios en archivos no seguidos (untracked files). Si no querés guardar estos cambios, podés usar:
```bash 
git stash -u
```
* Si sólo querés guardar los cambios en los archivos de seguimiento, puedes usar:
```bash 
git stash --keep-index
```
Esto guardará los cambios, pero mantendrá los archivos ya indexados (en stage) en tu área de trabajo.


---


## 🧪 Ejemplo práctico
Supón que estás trabajando en una nueva característica, pero necesitas cambiar a otra rama para revisar algo urgente. No quieres hacer un commit de tus cambios actuales, entonces puedes hacer lo siguiente:

1. Guarda los cambios actuales:
```bash 
git stash
```

2. Cambia a la rama urgente:
```bash 
git checkout otra-rama
```

3. Regresa a la rama original y aplica los cambios guardados:
```bash 
git checkout rama-original
git stash apply
```

---


`git stash` es una herramienta increíblemente útil cuando necesitas cambiar rápidamente de tarea sin comprometer cambios incompletos. Úsalo sabiamente para mejorar tu flujo de trabajo.


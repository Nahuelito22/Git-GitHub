# 📜 git log y git diff

Estos comandos nos permiten **ver el historial de cambios** y **comparar versiones**. Son esenciales para entender qué pasó y cuándo.

---

## 🕘 git log

Muestra un registro detallado de todos los commits realizados en el repositorio.

```bash
git log
```
Se ve algo como:
```bash
commit 3f5d3aa34...
Author: Nahuel Develop <nahuel@email.com>
Date:   Tue May 14 14:30:00 2025
     Añade sección de instalación en el README
```
 🔍 Opciones útiles:

* Mostrar en una línea:
```bash
git log --oneline
```

* Mostrar como gráfico de ramas:
```bash
git log --oneline --graph --all
```

* Limitar la cantidad de commits:
```bash
git log -n 5
```

---

## 🔍 git diff
Compara cambios entre versiones o entre el archivo actual y el último commit.
1. Ver cambios sin agregar (working directory vs último commit):
```bash
git diff
```

2. Ver cambios que ya están en staging:
```bash
git diff --staged
```

3. Comparar dos commits:
```bash
git diff hash1 hash2
```
* 📌 Podés obtener los hashes con git log.

---

💡 Tip: Para navegar el resultado de log o diff, usá las flechas ↑ ↓ y la tecla q para salir.

---

## 👀 Ejemplo práctico
```bash
# Ver historial
git log --oneline

# Ver qué cambió antes de hacer commit
git diff

# Ya agregaste los archivos con git add
git diff --staged
```
¡Estos comandos te ayudan a tener visibilidad total sobre los cambios en tu proyecto!

---

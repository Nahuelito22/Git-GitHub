# 📌 git add, commit y status

En esta sección vemos tres comandos clave del flujo de trabajo diario con Git: `add`, `commit` y `status`.

---

## 📥 git add

Este comando **prepara archivos para ser confirmados** (commit). Es decir, los mueve al "staging area".

```bash
git add nombre_del_archivo
```
📌 Para agregar todos los archivos modificados:

```bash
git add .
```
* ⚠️ ¡Ojo! Esto incluye todos los cambios: agregados, modificados y eliminados.

--- 

## 📦 git commit
Una vez que los archivos están en staging, usamos commit para guardar los cambios en el historial de versiones.

```bash
git commit -m "Mensaje descriptivo del cambio"
```
🧠 Consejo: Escribí mensajes claros y concisos. Ejemplo:
```bash
git commit -m "Agrega formulario de contacto y validación"
```

---

## 🔍 git status
Muestra el estado actual del repositorio: qué archivos han cambiado, cuáles están en staging y cuáles no.
```bash
git status
```
* Es muy útil para saber qué vas a confirmar antes de hacer commit.

---

## 🧠 Flujo básico
 1. Modificás archivos
 2. Preparás los cambios
git add archivo.txt
 3. Confirmás los cambios con un mensaje
git commit -m "Agrega archivo de configuración"

---

* 💡 Tip: Usá git status antes y después de hacer add para ver el efecto de tus comandos.

---


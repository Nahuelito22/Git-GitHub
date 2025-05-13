# 🔀 Merge y resolución de conflictos

Cuando trabajás con ramas, eventualmente vas a querer **fusionarlas** para integrar los cambios.  
Git lo permite mediante el comando `merge`.

---

## 🤝 ¿Qué es el merge?

Es el proceso de **unir dos ramas**. Generalmente se usa para llevar los cambios de una rama secundaria (como `feature`) a la rama principal (`main`).

---

## ✅ Hacer un merge

1. Cambiate a la rama donde querés aplicar los cambios (por ejemplo, `main`):

```bash
git checkout main
```

2. Ejecutá el merge:
```bash
git merge nombre-de-la-rama
```
* 💡 Esto trae los cambios de nombre-de-la-rama a main.

---

## 🧨 ¿Qué pasa si hay conflictos?
Si dos ramas modifican las mismas líneas en un archivo, Git no sabe cuál conservar y marca un conflicto.

---

## 💥 ¿Cómo se ve un conflicto?
Dentro del archivo con conflicto vas a ver algo así:
```bash
<<<<<<< HEAD
versión en main
=======
versión en rama-desarrollo
>>>>>>> rama-desarrollo
```
Debés elegir una versión, o combinarlas manualmente.

---

## 🛠️ ¿Cómo resolver conflictos?

1. Abrí los archivos marcados como conflictivos.

2. Editalos para quedarte con la versión deseada.

3. Guardá los cambios y hacé un commit:

```bash
git add archivo-conflicto.txt
git commit -m "Resuelto conflicto entre main y rama-desarrollo"
``` 

---

## 💡 Consejos para evitar conflictos
* Hacé pull antes de comenzar a trabajar.
* Comunicarse bien en equipos para no editar los mismos archivos.
* Hacer commits pequeños y frecuentes.

---

## 🧪 Ejemplo rápido

```bash
# Crear y cambiar a una rama
  git checkout -b nueva-funcionalidad

# Hacer cambios y commit...

# Volver a main
  git checkout main

# Mergear cambios
  git merge nueva-funcionalidad
```

---

Los conflictos son parte natural del trabajo en equipo. Aprender a resolverlos es clave para fluir con Git.


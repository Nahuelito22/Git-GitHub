# 🔀 Pull Requests (PR) en GitHub

Un **Pull Request** (PR) es una solicitud para fusionar los cambios realizados en una rama (por lo general, de un fork o feature branch) dentro de otra, como `main` o `develop`.

Es una herramienta clave para el trabajo colaborativo y revisión de código.

---

## 🧠 ¿Por qué usar Pull Requests?

- Permite revisar el código antes de integrarlo.
- Facilita comentarios, sugerencias y aprobaciones.
- Genera un historial claro de cambios.
- Favorece las buenas prácticas y calidad del código.

---

## 📥 Crear un Pull Request

1. Realizá tus cambios en una rama (puede ser local o desde un fork).
2. Subí la rama a GitHub con `git push origin tu-rama`.
3. En GitHub, hacé clic en el botón `Compare & pull request`.
4. Completá el título, descripción (explicando los cambios).
5. Asigná revisores, etiquetas, o vinculalo a un issue si corresponde.
6. Hacé clic en `Create Pull Request`.

---

## 🔍 Revisión de un PR

Una vez creado el PR:

- Los revisores pueden dejar comentarios sobre líneas específicas del código.
- Se puede aprobar o solicitar cambios.
- Se pueden hacer _commits_ adicionales en la misma rama para corregir lo pedido.

---

## ✅ Fusionar (merge) un Pull Request

Una vez aprobado:

1. Hacer clic en `Merge pull request`.
2. Elegir el tipo de fusión (Merge commit, Squash and merge, Rebase and merge).
3. Confirmar con `Confirm merge`.

> 💡 También se puede cerrar el PR sin fusionar si se considera innecesario.

---

## 🔄 Tipos de Merge

| Tipo               | Descripción                                                                 |
|--------------------|-----------------------------------------------------------------------------|
| Merge commit       | Fusiona manteniendo el historial completo.                                 |
| Squash and merge   | Une todos los commits en uno solo antes de fusionar.                       |
| Rebase and merge   | Reescribe el historial aplicando los commits uno por uno en el destino.    |

---

## 🔗 Asociar un PR a un Issue

En la descripción del PR, podés escribir:
* Closes #número_issue 

Esto cerrará automáticamente el issue al fusionar el PR.

---

## 🧩 Plantillas de PR

En proyectos grandes se pueden usar **Pull Request Templates** para estandarizar descripciones, checklist, etc.

---

> 🚀 Hacer Pull Requests claros y ordenados mejora la calidad del proyecto y la colaboración en equipo.

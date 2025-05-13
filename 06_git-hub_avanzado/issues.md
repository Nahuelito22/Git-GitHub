# 📝 Issues en GitHub

Los **issues** son herramientas clave para gestionar tareas, errores, sugerencias o mejoras dentro de un repositorio.  
Sirven como sistema de seguimiento colaborativo y transparente.

---

## 📌 ¿Para qué se usan los issues?

- Reportar errores o bugs.
- Sugerir nuevas funcionalidades.
- Discutir ideas o propuestas.
- Asignar tareas entre colaboradores.
- Documentar el progreso de un proyecto.

---

## 📝 Crear un issue

1. Ir a la pestaña `Issues` del repositorio.
2. Hacer clic en `New issue`.
3. Completar un título descriptivo y un comentario detallado.
4. Opcionalmente, podés:
   - Etiquetar (`labels`) el issue (ej: bug, enhancement, question).
   - Asignarlo a alguien (`assignees`).
   - Asociarlo a un proyecto o milestone.

> 💡 Es una buena práctica agregar capturas de pantalla, errores exactos o pasos para reproducir el problema.

---

## 🔖 Etiquetas comunes (`Labels`)

| Etiqueta       | Uso                                                              |
|----------------|------------------------------------------------------------------|
| `bug`          | Errores o fallos detectados.                                     |
| `enhancement`  | Sugerencias para mejorar una funcionalidad existente.            |
| `question`     | Dudas o solicitudes de ayuda.                                    |
| `documentation`| Problemas relacionados a la documentación.                       |
| `good first issue` | Ideal para principiantes que quieren contribuir.           |

---

## 👥 Asignar y colaborar en un issue

Podés comentar, compartir enlaces, mencionar a usuarios con `@usuario`, e incluso cerrar el issue desde un commit usando:

```bash
git commit -m "Arreglado el error en la validación de login. Closes #12"
```
Esto cerrará automáticamente el issue número 12 al hacer el push y merge.

---

## ✅ Cerrar un issue
Un issue puede cerrarse cuando:
* Se resuelve el problema.
* Se decide que no es relevante.
* Se fusiona un Pull Request relacionado.

---

## 🧩 Templates de Issues
Los repositorios grandes suelen tener plantillas (issue templates) para estandarizar el formato y facilitar la comprensión.

---

📢 Usar issues correctamente mejora la organización, comunicación y colaboración en proyectos de cualquier escala.


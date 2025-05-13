# ✅ Buenas Prácticas en Mensajes de Commit

Los mensajes de commit son una parte fundamental del trabajo con Git.  
No solo documentan qué cambios se hicieron, sino también **por qué** se hicieron.  
Un buen historial de commits ayuda a otros (y a vos mismo en el futuro) a entender la evolución del proyecto.

---

## 🧠 ¿Por qué importa escribir buenos commits?

- Facilita la revisión del código.
- Ayuda a encontrar errores o regresiones rápidamente.
- Permite generar changelogs automáticamente.
- Mejora el trabajo colaborativo.

---

## 📝 Estructura recomendada

Un mensaje de commit debería tener:

> <tipo>: <descripción breve> 

> [Descripción opcional más detallada, en presente y en modo imperativo.]

> [Si aplica, se puede agregar una referencia a un issue o ticket.]



---

## 🔖 Tipos comunes de commits (Convenciones)

| Tipo       | Uso                                                         |
|------------|-------------------------------------------------------------|
| `feat`     | Se agregó una nueva funcionalidad                          |
| `fix`      | Se corrigió un bug                                          |
| `docs`     | Cambios en la documentación                                |
| `style`    | Formato, espacios, comas, etc. (sin afectar lógica)        |
| `refactor` | Refactorización de código (sin cambiar funcionalidad)      |
| `test`     | Agregado o modificación de pruebas                         |
| `chore`    | Tareas menores o mantenimiento (build, configs, etc.)      |

---

## ✍️ Ejemplos de buenos commits
* feat: agregar botón para exportar reportes en PDF
* fix: corregir error al guardar usuarios sin email
* docs: actualizar sección de instalación en README
* refactor: extraer lógica de validación a un helper

> 💡 Usá el modo imperativo: "agregar", "corregir", "actualizar" en vez de "agregado", "corregido", "actualizado".

---

## 🚫 Malos ejemplos

* update cosas
* arreglos varios
* cambios
* asdfg

Estos no dicen nada útil y hacen más difícil entender el historial del proyecto.

---

## 📌 Bonus: Commits atómicos

Intentá que cada commit sea **atómico**, es decir:  
> Un solo cambio con un propósito claro.

Evitá commits enormes con múltiples cambios no relacionados. Es mejor dividirlos.

---

Con estas prácticas, tu historial de commits será claro, útil y profesional. ¡Te vas a agradecer a vos mismo más adelante!




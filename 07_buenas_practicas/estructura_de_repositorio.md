# 📁 Estructura de un Repositorio

Tener una estructura de repositorio clara y ordenada es fundamental para la mantenibilidad de un proyecto y la colaboración en equipo.  

Una buena estructura permite que cualquier persona entienda rápidamente dónde está cada parte del proyecto.

---

## 📦 Ejemplo de estructura típica en proyectos de software

```bash
mi-proyecto/
├── .gitignore
├── README.md
├── requirements.txt # o package.json, Pipfile, etc.
├── docs/ # Documentación del proyecto
├── src/ # Código fuente
│ ├── main.py
│ └── módulos/
├── tests/ # Pruebas automáticas
│ └── test_main.py
└── assets/ # Imágenes, logos, etc.
```

---

## 🧹 Buenas prácticas

- Usar nombres **claros y descriptivos** para carpetas y archivos.
- Mantener un archivo `README.md` actualizado con información del proyecto.
- Incluir un `.gitignore` para evitar subir archivos innecesarios.
- Separar el código fuente (`src/`) de los tests (`tests/`).
- Si usás dependencias, agregá un archivo como `requirements.txt`, `package.json`, etc.
- Si tenés documentación extensa, crear una carpeta `docs/`.

---

## 🧾 README.md bien estructurado

Tu `README.md` debería incluir:

- Nombre y descripción del proyecto
- Cómo instalar y correr el proyecto
- Ejemplos de uso
- Tecnologías utilizadas
- Créditos y licencias

> 💡 Consejo: Un buen `README.md` es la carta de presentación de tu repositorio.

---

## 🧱 Otras carpetas útiles

| Carpeta     | Uso                                     |
|-------------|------------------------------------------|
| `config/`   | Configuraciones específicas del entorno |
| `data/`     | Archivos de datos de entrada/salida     |
| `scripts/`  | Scripts útiles para tareas repetitivas  |
| `notebooks/`| Jupyter Notebooks (en proyectos de data)|

---

Mantener una estructura limpia y coherente facilita el trabajo colaborativo, la comprensión del código y la escalabilidad del proyecto.


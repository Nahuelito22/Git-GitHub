# 🌿 ¿Qué es Git Flow?

**Git Flow** es un modelo de ramificación propuesto por Vincent Driessen que define una estructura clara para trabajar en proyectos colaborativos.  
Ayuda a organizar mejor el desarrollo de software y manejar versiones de forma profesional.

---

## 🔀 Principales ramas en Git Flow

| Rama         | Propósito                                                                 |
|--------------|---------------------------------------------------------------------------|
| `main`       | Contiene el código de producción, estable y listo para ser lanzado.       |
| `develop`    | Código en desarrollo. Acá se integran las nuevas funcionalidades.         |
| `feature/*`  | Ramas temporales para desarrollar nuevas funcionalidades.                 |
| `release/*`  | Preparan nuevas versiones para producción. Permiten pruebas y ajustes.    |
| `hotfix/*`   | Usadas para corregir errores críticos directamente en producción.         |

---

## 🧭 Flujo de trabajo paso a paso

1. **Clonar el repositorio:**

```bash
git clone https://github.com/usuario/mi-repo.git
cd mi-repo
```

2. Crear una nueva funcionalidad:
```bash
git checkout develop
git checkout -b feature/nueva-funcionalidad
```

3. Desarrollar y hacer commits.
* Luego, integrar con develop:
```bash
git checkout develop
git merge feature/nueva-funcionalidad
git branch -d feature/nueva-funcionalidad
```

4. Crear una rama release cuando se termina una versión:
```bash
git checkout -b release/v1.0
```
Acá podés corregir bugs menores, actualizar documentación, etc.

5. Finalizar la release:
```bash
git checkout main
git merge release/v1.0
git tag -a v1.0 -m "Versión 1.0"
git checkout develop
git merge release/v1.0
git branch -d release/v1.0
```

6. Corregir errores en producción (hotfix):
```bash
git checkout main
git checkout -b hotfix/bug-critico
```
Luego:
```bash
git commit -m "Fix: corrige error crítico"
git checkout main
git merge hotfix/bug-critico
git checkout develop
git merge hotfix/bug-critico
git branch -d hotfix/bug-critico
```

---

## ✅ Ventajas de usar Git Flow

* Organización clara.
* Permite trabajar en paralelo.
* Facilita el versionado semántico (v1.0, v1.1, etc.).
* Ideal para equipos medianos o grandes.

---

## ⚠️ ¿Cuándo evitarlo?

* Proyectos muy simples o individuales.
* Casos donde el desarrollo es muy rápido y no requiere tanto control.

---

 💡 Consejo: Podés automatizar este flujo usando la extensión de consola git-flow, aunque no es obligatorio.
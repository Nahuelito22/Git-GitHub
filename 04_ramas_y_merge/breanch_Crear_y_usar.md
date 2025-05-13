# 🌿 Crear y usar ramas (branches)

Las ramas en Git permiten desarrollar funcionalidades **aisladamente**, sin afectar la rama principal (`main` o `master`).

---

## 🧠 ¿Qué es una rama?

Una **rama** es como una línea paralela de trabajo. Podés usarla para:
- Desarrollar nuevas funcionalidades.
- Hacer pruebas sin romper el código principal.
- Organizar mejor tu flujo de trabajo.

---

## 🌱 Crear una nueva rama

```bash
git branch nombre-de-la-rama
```
Esto solo la crea, no te cambia a ella.

---

## 🔀 Cambiarse a una rama

```bash
git checkout nombre-de-la-rama
```

* ✅ A partir de Git 2.23 podés usar:

```bash
git switch nombre-de-la-rama
```

---

## 🛠️ Crear y cambiarse a la rama (todo junto)
```bash
git checkout -b nombre-de-la-rama
```

* ✅ Alternativa moderna:
```bash
git switch -c nombre-de-la-rama
```

---

## 📋 Listar ramas

```bash
git branch
```
* La rama actual se muestra con un asterisco *.


---


## 🧹 Eliminar una rama
```bash
git branch -d nombre-de-la-rama
```
* ⚠️ Si la rama no fue fusionada, usá -D para forzar su eliminación.

---

## 💡 Tips útiles
* Mantené los nombres de ramas descriptivos, por ejemplo: feature/form-contacto, bugfix/login-error, hotfix/logo-mobile.
* Evitá trabajar directamente en main a menos que sea necesario.
* Siempre mergeá los cambios importantes en main para que no se pierdan.


---


## 🧪 Ejemplo rápido

```bash
# Crear una rama
  git branch desarrollo

# Cambiarse a la rama
  git checkout desarrollo

# Hacer cambios, luego commit...

# Volver a main
  git checkout main
```
---

Usar ramas te permite trabajar de forma más ordenada y profesional, especialmente en equipo. 🚀
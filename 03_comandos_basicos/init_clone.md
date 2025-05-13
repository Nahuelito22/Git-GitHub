# 🚀 Git Init y Clone

En esta sección veremos cómo empezar un proyecto nuevo con Git (`git init`) o cómo clonar uno ya existente desde un repositorio remoto (`git clone`).

---

## 🧱 git init

Este comando se usa para **inicializar un repositorio Git local**. Es ideal cuando estás comenzando un proyecto desde cero en tu máquina.

```bash
git init
```
Esto crea una carpeta oculta .git que le dice a Git que empiece a rastrear los cambios en el directorio.

📌 Ejemplo:
```bash
mkdir mi_proyecto
cd mi_proyecto
git init
```

---

## 🌐 git clone
Se utiliza para clonar un repositorio existente desde GitHub (u otro servidor Git) a tu máquina local.

```bash
git clone URL_DEL_REPO
```

📌 Ejemplo con HTTPS:

```bash
git clone https://github.com/usuario/repositorio.git
```

📌 Ejemplo con SSH:

```bash
git clone git@github.com:usuario/repositorio.git
```

Esto descarga todos los archivos del proyecto y su historial de versiones.

---

## ✅ Diferencias principales

| Comando     | Uso principal                               |
| ----------- | ------------------------------------------- |
| `git init`  | Crear un nuevo repositorio local desde cero |
| `git clone` | Copiar un repositorio remoto existente      |


---

## 🔍 Tip extra
Si querés clonar el repo en una carpeta con otro nombre:

```bash
git clone https://github.com/usuario/repositorio.git mi-carpeta-personalizada
```
---
💡 Consejo: Usá git init cuando estés creando algo nuevo, y git clone cuando estés colaborando en algo que ya existe.
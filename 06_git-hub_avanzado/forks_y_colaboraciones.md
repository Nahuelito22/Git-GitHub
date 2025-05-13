# 🍴 Forks y Colaboraciones en GitHub

GitHub facilita mucho el trabajo en equipo. Una de las formas más comunes de colaborar con otros proyectos es a través de los **forks**.

---

## 🔄 ¿Qué es un fork?

Un **fork** es una copia de un repositorio ajeno que se crea en tu propia cuenta de GitHub.  
Te permite experimentar libremente con cambios sin afectar el repositorio original.

> 📦 Ideal para contribuir a proyectos de código abierto.

---

## 👣 ¿Cómo hacer un fork?

1. Entrá al repositorio que te interesa.
2. Hacé clic en el botón `Fork` (arriba a la derecha).
3. GitHub creará una copia del repositorio en tu cuenta.

---

## ⬇️ Cloná tu fork localmente

```bash
git clone https://github.com/tu-usuario/repositorio-forkeado.git
cd repositorio-forkeado
```

---

## 🔄 Sincronizá tu fork con el repo original (opcional)
Agregá el repositorio original como un remoto:
```bash
git remote add upstream https://github.com/usuario-original/repositorio.git
```

Traé los cambios del original:
```bash
git fetch upstream
```

Fusioná los cambios del original con tu rama actual:
```bash
git merge upstream/main
```

---

## 🧑‍🤝‍🧑 Colaboración a través de forks
1. Hacés cambios en tu fork (en una rama nueva si es posible).
2. Subís los cambios a tu repositorio.
3. Desde GitHub, creás un Pull Request al repositorio original.

---

## ✅ Buenas prácticas
* Usá ramas descriptivas, por ejemplo: fix/error-login, feature/formulario-contacto
* Hacé commits claros y ordenados.
* Verificá que tu código no rompa funcionalidades existentes.

---

## ❗ Diferencia entre fork y clone
| Acción  | ¿Qué hace?                                                                    |
| ------- | ----------------------------------------------------------------------------- |
| `clone` | Crea una copia local de un repositorio (puede ser tuyo o de otro usuario).    |
| `fork`  | Crea una copia completa en tu cuenta de GitHub, para luego clonar o trabajar. |


---

💡 Los forks son una herramienta poderosa para colaborar sin necesidad de tener permisos de escritura en el proyecto original.
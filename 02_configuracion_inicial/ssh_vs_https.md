# 🔐 SSH vs HTTPS en GitHub

---

## 🤔 ¿Qué son SSH y HTTPS?

Cuando trabajás con Git y GitHub, tenés dos formas principales de autenticarte al clonar repositorios o hacer push:

- **HTTPS:** Usás tu nombre de usuario y contraseña/token cada vez que interactuás con el repositorio.
- **SSH:** Usás una clave pública y privada para autenticarte sin necesidad de ingresar usuario/contraseña.

---

## 🌐 HTTPS

### ✅ Ventajas:

- Más simple de configurar para principiantes.
- No requiere generación de claves.

### ❌ Desventajas:

- Necesitás ingresar tus credenciales o token personal cada vez (o usar un gestor de credenciales).

### Ejemplo de URL HTTPS:
https://github.com/usuario/repositorio.git


---

## 🔐 SSH

### ✅ Ventajas:

- Una vez configurado, no necesitás ingresar credenciales cada vez.
- Más seguro para proyectos frecuentes o trabajo en equipo.

### ❌ Desventajas:

- Requiere configuración inicial de claves SSH.
- Puede ser bloqueado por algunos firewalls/restricciones de red.

### Ejemplo de URL SSH:
git@github.com:usuario/repositorio.git

---

## ⚙️ Cómo generar y usar una clave SSH

1. Generá una nueva clave (si no tenés una):

```bash
ssh-keygen -t ed25519 -C "tu-correo@ejemplo.com"
```
* Si tu sistema no soporta ed25519, podés usar rsa:
```bash
ssh-keygen -t rsa -b 4096 -C "tu-correo@ejemplo.com"
```
2. Presioná Enter para aceptar la ubicación por defecto.
3. Agregá la clave al agente SSH:
```bash
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
```
4.Copiá la clave pública al portapapeles:
```bash
cat ~/.ssh/id_ed25519.pub
```
5. Pegala en GitHub:
* Ir a GitHub → Settings → SSH and GPG keys
* Hacé clic en "New SSH key" y pegá la clave pública.

---

## 🧪 Probar la conexión SSH
```bash
ssh -T git@github.com
```
Si todo está bien, verás un mensaje como:
```bash
Hi tu-usuario! You've successfully authenticated, but GitHub does not provide shell access.

```
---
## 🧭 ¿Cuál elegir?
| Situación                       | Recomendación |
| ------------------------------- | ------------- |
| Principiante o usos esporádicos | HTTPS         |
| Uso frecuente o profesional     | SSH           |
| Red con restricciones           | HTTPS         |

* 🎯 Recomendación: Aprendé ambas, usá HTTPS si querés algo rápido, y SSH si querés mayor comodidad a largo plazo.

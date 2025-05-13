# Instalación y configuración inicial de Git

## 📥 Instalación de Git

### En Windows

1. Entrá a: https://git-scm.com/download/win  
2. Se descargará automáticamente el instalador.  
3. Ejecutá el instalador y dejá todo por defecto (a menos que sepas lo que estás cambiando).  
4. Finalizá la instalación y abrí **Git Bash** (se instala junto con Git).

### En Linux (Debian/Ubuntu)

```bash
sudo apt update
sudo apt install git 
```


### En macOS
Usá Homebrew para instalar Git

```bash
brew install git 
```
Verificaar la instalación con:

```bash
git --version
```

## 🛠️ Configuración Inicial
Después de instalar Git, es buena práctica configurarlo con tu nombre y correo (serán visibles en tus commits).

```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tuemail@ejemplo.com"
```
✅ El flag --global indica que estas configuraciones se aplican a todos los repositorios del sistema.
Si querés una configuración distinta para un solo proyecto, omitilo y ejecutá los comandos dentro del repositorio.


También podés configurar el editor de texto por defecto (opcional):

```bash
git config --global core.editor "code --wait"
# Este ejemplo configura Visual Studio Code como editor por defecto.
```
## 🔍 Ver y Modificar Configuraciones
* Para ver la configuración actual:
```bash
git config --list
```
* Para ver un dato específico:
```bash
git config user.name
git config user.email
```

* Para editar el archivo de configuración global manualmente:
```bash
code ~/.gitconfig
```
💡 Podés reemplazar code por el editor que uses (nano, vim, notepad, etc.).


# 04. Instalación, Configuración y Autenticación

[⬅️ Módulo Anterior: Fundamentos de GitHub](./03-fundamentos-de-github.md) | [🏠 Volver al Índice](./README.md) | [Siguiente Módulo: Chuleta de Comandos ➡️](./05-chuleta-comandos-git.md)


## 💻 1. Instalación de Git

### Windows
1. Descarga el instalador oficial desde [git-scm.com/download/win](https://git-scm.com/download/win).
2. Ejecuta el instalador. Durante el asistente, se recomienda:
   - Mantener **Git Bash** seleccionado.
   - Elegir como editor predeterminado **VS Code** o **Nano**.
   - Seleccionar **"Override the default branch name for new repositories"** y nombrarla `main`.
   - Elegir **"Checkout Windows-style, commit Unix-style line endings"** (`core.autocrlf = true`).

### macOS
Puedes instalarlo mediante [Homebrew](https://brew.sh/) o las herramientas de Xcode:
```bash
# Con Homebrew (Recomendado)
brew install git

# O mediante Xcode Command Line Tools
xcode-select --install
```

### Linux (Ubuntu / Debian / Fedora / Arch)
```bash
# Ubuntu / Debian
sudo apt update && sudo apt install git -y

# Fedora / RHEL
sudo dnf install git -y

# Arch Linux
sudo pacman -S git
```

### 🔍 Verificar instalación
Abre tu terminal y ejecuta:
```bash
git --version
# Ejemplo de salida: git version 2.45.0
```


## ⚙️ 2. Configuración Inicial Obligatoria (`git config`)

Git necesita saber quién eres para firmar cada uno de tus commits. Configura tu identidad globalmente:

```bash
# 1. Tu nombre real o tu nombre de usuario/alias (ej. "Ana García" o "anadev")
git config --global user.name "Tu Nombre o Usuario"

# 2. Tu correo electrónico (debe coincidir con el de tu cuenta de GitHub)
git config --global user.email "tu_email@ejemplo.com"

# 3. Establecer 'main' como la rama inicial por defecto
git config --global init.defaultBranch main

# 4. Configurar tu editor de texto preferido (ej. VS Code)
git config --global core.editor "code --wait"

# 5. Tratamiento de saltos de línea (Windows: true | Mac/Linux: input)
# En Windows:
git config --global core.autocrlf true
# En macOS / Linux:
git config --global core.autocrlf input
```

> [!TIP]
> **💡 ¿Debo poner las comillas (`" "`) o no?**
> - **Obligatorias si hay espacios**: Si pones tu nombre y apellido (ej. `"Ana García"`) o comandos con argumentos (`"code --wait"`). Si no pones comillas, la terminal pensará que el apellido es un comando separado y fallará.
> - **Opcionales si no hay espacios**: Si usas un nombre de usuario/alias único (ej. `anadev` o `"anadev"`) o tu correo (`usuario@gmail.com` o `"usuario@gmail.com"`), ambas formas funcionan exactamente igual.
> - **Sin comillas**: Para valores de configuración del sistema como `true`, `false`, `main` o `input`.

### 📋 Verificar tu configuración activa
```bash
git config --list --show-origin
```


## 🔐 3. Cómo Conectar tu Computadora con GitHub (Autenticación)

> [!NOTE]
> Por seguridad, **GitHub ya no permite usar tu contraseña habitual de cuenta al hacer `git push`**. En su lugar, el proceso se ha vuelto automático y mucho más sencillo.

### 🌟 Opción 1: Inicio de Sesión Automático con el Navegador (La más fácil)

Cuando instales Git en Windows o macOS, ya viene incluido **Git Credential Manager**.

La primera vez que intentes subir código a GitHub (`git push`), **se abrirá automáticamente una ventana emergente** preguntándote cómo deseas iniciar sesión:

```
┌─────────────────────────────────────────────────────────────┐
│                    Sign in to GitHub                        │
│                                                             │
│   🌐 [ Sign in with your browser ]  <-- (RECOMENDADO)       │
│                                                             │
│   🔢 [ Sign in with a code ]                                │
│                                                             │
│   🔑 [ Token ]                                              │
└─────────────────────────────────────────────────────────────┘
```

- **Si eliges `Sign in with your browser` (Recomendado)**:
  1. Se abrirá una pestaña en tu navegador web.
  2. Haz clic en el botón verde **"Authorize GitCredentialManager"**.
  3. ¡Listo! La ventana se cerrará sola y tu computadora recordará el acceso para siempre.

- **Si eliges `Sign in with a code`**:
  1. Git te mostrará un código de 8 caracteres (ej. `ABCD-1234`).
  2. Entra a [github.com/login/device](https://github.com/login/device) en tu navegador, pega el código y confirma.


### 💻 Opción 2: Autenticación con GitHub CLI (`gh`)

Si prefieres hacerlo todo desde la terminal:
```bash
gh auth login
```
Selecciona `GitHub.com` ➔ `HTTPS` ➔ `Login with a web browser` y confirma en tu navegador.


### 🔑 Opción 3: Claves SSH (Para usuarios avanzados o servidores)

<details>
<summary><strong>👉 Haz clic aquí si necesitas configurar Claves SSH</strong></summary>

Las claves SSH son útiles si trabajas en servidores Linux remotos o prefieres no depender del navegador:

1. **Generar clave SSH:**
   ```bash
   ssh-keygen -t ed25519 -C "tu_email@ejemplo.com"
   ```
2. **Copiar clave pública:**
   - En Windows (Git Bash): `clip < ~/.ssh/id_ed25519.pub`
   - En macOS: `pbcopy < ~/.ssh/id_ed25519.pub`
   - En Linux: `cat ~/.ssh/id_ed25519.pub`
3. **Pegarla en GitHub:**
   - Ve a **GitHub Settings** ➔ **SSH and GPG keys** ➔ **New SSH Key**.
4. **Probar conexión:**
   ```bash
   ssh -T git@github.com
   ```

</details>


## 🚫 4. El Archivo `.gitignore`: Evita Subir Basura o Secretos

El archivo `.gitignore` le indica a Git qué archivos o carpetas debe ignorar intencionalmente en tu proyecto.

> [!CAUTION]
> **Nunca subas a GitHub:**
> - Archivos con credenciales o claves API (`.env`, `credentials.json`).
> - Dependencias pesadas (`node_modules/`, `venv/`, `vendor/`).
> - Archivos temporales del sistema (`.DS_Store`, `Thumbs.db`).
> - Archivos de compilación (`dist/`, `build/`, `*.exe`, `*.log`).

### Ejemplo de archivo `.gitignore`:
```gitignore
# Variables de entorno y secretos
.env
.env.local
*.pem
*.key

# Dependencias
node_modules/
vendor/
__pycache__/
*.pyc

# Archivos del sistema y de editores
.DS_Store
Thumbs.db
.vscode/
.idea/

# Carpetas de construcción y logs
dist/
build/
*.log
```

> [!TIP]
> Puedes generar plantillas completas de `.gitignore` para cualquier lenguaje o framework en [gitignore.io](https://www.toptal.com/developers/gitignore).


## 🚀 5. Crear y Subir tu Primer Proyecto a GitHub

Para comenzar un proyecto y subirlo a GitHub existen diferentes formas según tus preferencias. Elige la **Ruta Local** que más te guste y luego sigue los pasos para conectarlo con GitHub:

### Fase 1: Abrir tu proyecto local (Elige una ruta)

#### 🔹 Ruta A: Con VS Code (La más visual y recomendada)
1. Crea tu carpeta en el explorador de archivos (ej. `mi-primer-proyecto`).
2. Haz clic derecho sobre la carpeta ➔ **"Abrir con Code"** (o arrastra la carpeta dentro de VS Code).
3. Abre la terminal integrada de VS Code con el atajo `Ctrl + Ñ` ( o `Ctrl + ` ` ` / menú *Terminal ➔ New Terminal*).

> [!TIP]
> **¿Qué terminal usar dentro de VS Code (Windows)?**
> En la esquina superior derecha del panel de terminal de VS Code puedes elegir qué consola usar:
> - **Recomendado**: Selecciona **Git Bash** o **Símbolo del sistema (CMD)**.
> - **Evita PowerShell** si te aparece el típico error en rojo de Windows: *"la ejecución de scripts está deshabilitada en este sistema"*.

#### 🔹 Ruta B: Desde el Explorador de Archivos + Terminal externa
1. Crea y entra a tu carpeta en el explorador de archivos.
2. Haz clic derecho en cualquier espacio vacío ➔ **"Abrir en Terminal"** o **"Git Bash Here"** (o haz clic en la barra de direcciones de la carpeta, escribe `cmd` y presiona `Enter`).

#### 🔹 Ruta C: 100% desde la Terminal (Solo comandos)
1. Abre tu terminal favorita (Git Bash, CMD, Terminal de Mac/Linux).
2. Crea la carpeta y entra en ella con comandos:
   ```bash
   mkdir mi-primer-proyecto
   cd mi-primer-proyecto
   code . # (Opcional: abre VS Code en esta carpeta)
   ```


### Fase 2: Crear el repositorio en la página web de GitHub (con clics)

1. Inicia sesión en [GitHub.com](https://github.com).
2. Haz clic en el botón verde **"New"** (o en el ícono `+` arriba a la derecha ➔ **New repository**).
3. Escribe el nombre de tu repositorio (ej. `mi-primer-proyecto`).
4. Selecciona si será **Público** o **Privado**.
5. ⚠️ **MUY IMPORTANTE**: **NO marques** las opciones de *"Add a README file"*, *"Add .gitignore"* ni *"Choose a license"*. Necesitamos que el repositorio esté vacío para recibir tus archivos locales.
6. Haz clic en el botón verde **"Create repository"**.


### Fase 3: Conectar y subir tu código local a GitHub

En la terminal que abriste en la **Fase 1**, ejecuta los siguientes comandos en orden (reemplaza `tuusuario` y `mi-primer-proyecto` con los datos de tu repositorio):

```bash
# 1. Inicializar Git en tu carpeta
git init

# 2. Preparar todos tus archivos para guardar
git add .

# 3. Guardar tu primer commit
git commit -m "feat: primer commit de mi proyecto"

# 4. Asegurar que la rama principal se llame 'main'
git branch -M main

# 5. Vincular tu carpeta local con el repositorio de GitHub
git remote add origin https://github.com/tuusuario/mi-primer-proyecto.git

# 6. Subir tus archivos a GitHub
git push -u origin main
```

*(Si es tu primera vez, en el último paso se abrirá automáticamente la ventana de inicio de sesión de GitHub; haz clic en **Sign in with your browser** para autorizar).*

---

[⬅️ Módulo Anterior: Fundamentos de GitHub](./03-fundamentos-de-github.md) | [🏠 Volver al Índice](./README.md) | [Siguiente Módulo: Chuleta de Comandos ➡️](./05-chuleta-comandos-git.md)

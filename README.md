<div align="center">

<img width="180" src="https://raw.githubusercontent.com/monochrome-music/monochrome/main/public/icon-512.png" />

# 🎵 Fabiodalez Music

### Android Music Streaming App basada en Monochrome 🚀

<p align="center">
  <b>Fabiodalez Music</b> es una aplicación Android diseñada como wrapper nativo para Monochrome, enfocada en ofrecer una experiencia moderna de streaming musical con privacidad, reproducción en segundo plano y funcionalidades multimedia avanzadas.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Android-Mobile%20App-3DDC84?style=for-the-badge&logo=android">
  <img src="https://img.shields.io/badge/Java-Native%20Bridge-orange?style=for-the-badge&logo=openjdk">
  <img src="https://img.shields.io/badge/Capacitor-Hybrid%20App-119EFF?style=for-the-badge&logo=capacitor">
  <img src="https://img.shields.io/badge/Open%20Source-Music-success?style=for-the-badge">
</p>

<p align="center">
  <a href="#-preview">Preview</a> •
  <a href="#-características">Características</a> •
  <a href="#-arquitectura">Arquitectura</a> •
  <a href="#-instalación">Instalación</a> •
  <a href="#-roadmap">Roadmap</a>
</p>

</div>

---

# 🌌 Acerca del Proyecto

**Fabiodalez Music** es una aplicación Android híbrida construida sobre el proyecto open source Monochrome.

La aplicación combina:

- 🎵 Streaming musical
- 📱 Funcionalidades Android nativas
- 🔒 Privacidad del usuario
- ⚡ Reproducción avanzada
- 🎧 Integración multimedia
- 🚀 Experiencia moderna

El proyecto está orientado al aprendizaje y práctica de:

- Android Development
- Capacitor
- Java nativo
- Bridges híbridos
- Multimedia APIs
- Servicios foreground
- Aplicaciones musicales

---

# 📸 Preview

<div align="center">

<img width="700" src="https://raw.githubusercontent.com/monochrome-music/monochrome/main/public/icon-512.png"/>

</div>

---

# ✨ Características

## 🎵 Reproducción Multimedia

- ▶️ Reproducción en segundo plano
- 🎧 Controles multimedia nativos
- 🔊 Compatibilidad Bluetooth
- ⏸️ Auto pausa por desconexión Bluetooth
- 📲 Integración con pantalla de bloqueo

---

## 📥 Gestión de Descargas

- 💾 Descarga de canciones
- 📂 Guardado automático en:

```bash
Downloads/FabiodalezMusic/
```

- 🔔 Notificaciones Android nativas
- ⚡ Manejo optimizado de archivos

---

## 📱 Funciones Android Nativas

- 📂 Selector de carpetas musicales
- 📋 Integración con portapapeles
- 🌐 OAuth mediante Chrome Custom Tabs
- 🔋 Bypass de optimización de batería
- 🔥 Servicios foreground

---

## 🎨 Interfaz y UX

- ✨ Branding personalizado
- 🌙 Safe area support
- 📲 Barra de navegación visible
- 🔙 Navegación optimizada
- 🚀 Experiencia fluida

---

# 🛠️ Tecnologías Utilizadas

## 📱 Mobile Development

<p>
  <img src="https://skillicons.dev/icons?i=androidstudio,java,javascript,typescript" />
</p>

- Android
- Java
- JavaScript
- TypeScript

---

## ⚙️ Frameworks y Herramientas

<p>
  <img src="https://skillicons.dev/icons?i=nodejs,git,github,vscode" />
</p>

- Capacitor
- Monochrome
- Node.js
- Git & GitHub

---

# 📂 Estructura del Proyecto

```bash
Fabiodalez-Music/
│
├── android/                  # Código nativo Android
├── android-service.js        # Bridge JavaScript
├── capacitor.config.ts       # Configuración Capacitor
├── build-android.sh          # Script de compilación
├── install.sh                # Instalador overlay
├── patches/                  # Parches temporales
└── README.md
```

---

# ⚡ Instalación

# 🛠️ Requisitos

## Software necesario

- macOS
- Homebrew
- JDK 21
- Android SDK Tools

---

## 1️⃣ Instalar dependencias

```bash
brew install openjdk@21
```

```bash
brew install --cask android-commandlinetools
```

---

## 2️⃣ Clonar Monochrome

```bash
git clone https://github.com/monochrome-music/monochrome.git
```

```bash
cd monochrome
```

```bash
git remote rename origin upstream
```

---

## 3️⃣ Clonar overlay Android

```bash
git clone https://github.com/fabiodalez-dev/Monochrome-Android-APK
```

---

## 4️⃣ Instalar overlay

```bash
cd Monochrome-Android-APK
```

```bash
chmod +x install.sh
```

```bash
./install.sh ../monochrome
```

---

## 5️⃣ Compilar APK

```bash
cd ../monochrome
```

```bash
./build-android.sh
```

---

# 📦 APK Generado

El APK final estará disponible en:

```bash
Monochrome-debug.apk
```

---

# 🔄 Actualizaciones

## 🚀 Actualizar Monochrome

```bash
cd monochrome
```

```bash
./build-android.sh
```

El sistema automáticamente:

- 🔥 Descarga cambios upstream
- ⚡ Aplica parches
- 📦 Genera APK
- 🧹 Restaura archivos originales

---

# 🧠 Cómo Funciona

## ⚡ Sistema de Parches

Durante la compilación se modifican temporalmente:

- `index.html`
- `package.json`

---

## 🔥 Bridges Android

La lógica Android vive completamente en:

```bash
android/
android-service.js
capacitor.config.ts
build-android.sh
```

---

# 🏗️ Arquitectura

```bash
Monochrome (Web App)
    │
    ├── Capacitor WebView
    │
    ├── android-service.js
    │   ├── Media Controls
    │   ├── Download Handler
    │   ├── CSS Injection
    │   ├── Back Navigation
    │   ├── Clipboard Bridge
    │   └── OAuth Bridge
    │
    └── Native Java
        ├── AudioForegroundService
        ├── AudioServicePlugin
        ├── DownloadBridge
        ├── LocalFilesBridge
        └── AndroidBridge
```

---

# 🔥 Funcionalidades Técnicas

## 🎧 Media Controls

- Notification controls
- Lock screen controls
- Bluetooth integration
- MediaSession support

---

## 📥 Descargas

- MediaStore integration
- Native Android saving
- Notification support
- Download handling bridge

---

## 🌐 OAuth

- Chrome Custom Tabs
- Native browser integration
- Secure authentication flow

---

# 🧠 Objetivos del Proyecto

## 🎯 Aprender y practicar

- Android híbrido
- Capacitor
- Bridges nativos
- Multimedia APIs
- Servicios Android
- Audio playback
- Integración WebView
- Automatización de builds

---

# 📊 Roadmap

## 🚧 Próximamente

- 🎶 Equalizer avanzado
- 🌙 Dark mode dinámico
- ☁️ Sync multiplataforma
- ❤️ Favoritos offline
- 📱 Widgets Android
- 🔥 Android Auto support
- 🎧 Visualizador de audio
- 🚀 Optimización de rendimiento

---

# 🤝 Contribuciones

Las contribuciones son bienvenidas ❤️

## Pasos para contribuir

1. Haz Fork del proyecto
2. Crea una rama

```bash
git checkout -b feature/nueva-funcion
```

3. Realiza tus cambios
4. Haz commit

```bash
git commit -m "✨ Nueva funcionalidad"
```

5. Haz push

```bash
git push origin feature/nueva-funcion
```

6. Abre un Pull Request 🚀

---

# 🙌 Créditos

- 🎵 Monochrome Music
- ⚡ Capacitor Team
- 🤖 Android Developers
- 🚀 Comunidad Open Source

---

# 👨‍💻 Autor

<div align="center">

<img src="https://github.com/isairey.png" width="120" style="border-radius:50%" />

## Android & Hybrid App Developer

Apasionado por aplicaciones musicales, Android nativo y experiencias multimedia modernas.

</div>

---

# 🌟 Apoya el Proyecto

Si te gusta Fabiodalez Music:

⭐ Dale una estrella al repositorio  
🍴 Haz Fork del proyecto  
📢 Compártelo con otros desarrolladores

---

# ☕ Buy Me a Coffee

<p align="center">

<a href="https://buymeacoffee.com/fabiodalez">
  <img src="https://img.shields.io/badge/Buy%20Me%20a%20Coffee-ffdd00?style=for-the-badge&logo=buy-me-a-coffee&logoColor=black">
</a>

</p>

---

# 📜 Licencia

Este proyecto utiliza la misma licencia que Monochrome.

---

<div align="center">

### 🎵 Fabiodalez Music — Android, privacidad y música en una experiencia moderna.

</div>

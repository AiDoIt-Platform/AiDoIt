<div align="center">

<img src="assets/aidoit-readme-cover.png" alt="AiDoIt unifica proveedores, modelos y herramientas de programación con IA" width="100%" />

<br />

[简体中文](README.md) · [English](README.en.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Deutsch](README.de.md) · [العربية](README.ar.md) · [Español](README.es.md)

<br />

[![Versión](https://img.shields.io/badge/Release-v0.0.9-7c3aed?style=for-the-badge)](https://github.com/AiDoIt-Platform/AiDoIt/releases/latest)
[![Windows](https://img.shields.io/badge/Windows-10%20%7C%2011-0ea5e9?style=for-the-badge&logo=windows11&logoColor=white)](https://github.com/AiDoIt-Platform/AiDoIt/releases/latest)
[![Ubuntu](https://img.shields.io/badge/Ubuntu-x64%20%7C%20ARM64-e95420?style=for-the-badge&logo=ubuntu&logoColor=white)](HelpMd/Ubuntu/README.md)
[![Privacidad](https://img.shields.io/badge/API_Keys-solo_local-10b981?style=for-the-badge)](#-seguridad-y-privacidad)
[![Licencia](https://img.shields.io/badge/License-GPLv3-f59e0b?style=for-the-badge)](LICENSE)

### Una aplicación para tus herramientas y modelos de programación con IA

AiDoIt admite **Windows y Ubuntu x64 / ARM64**. Administra **Codex, ChatGPT, Claude Code, Claude Desktop y DeepSeek Harness** en Windows, despliega Codex y Claude Code en servidores Ubuntu y alterna entre cuentas oficiales y modelos externos.

[Descargar](https://github.com/AiDoIt-Platform/AiDoIt/releases/latest) · [Inicio rápido](#-inicio-rápido) · [Guías visuales](#-documentación) · [Informar de un problema](https://github.com/AiDoIt-Platform/AiDoIt/issues/new)

</div>

---

## ✨ Por qué elegir AiDoIt

| Capacidad | Qué obtienes |
|---|---|
| **Windows + Ubuntu** | Compatible con Windows 10/11 y entornos CLI de Ubuntu x64 / ARM64 |
| **Un único panel** | Administra Codex, Claude y DeepSeek Harness sin editar archivos de configuración continuamente |
| **Detección automática** | Encuentra aplicaciones, CLI, sesiones iniciadas y entornos locales |
| **Varios proveedores y modelos** | Mantiene separados proveedores, credenciales y catálogos de modelos |
| **Prueba antes de activar** | Comprueba la disponibilidad y el tiempo de respuesta real de cada modelo |
| **Configuración aislada** | Codex, Claude y Harness se administran por separado y no interfieren entre sí |
| **Restauración segura** | Guarda el estado original y restaura la configuración oficial al desactivar el acceso |
| **Actualización integrada** | Desde `v0.0.7`, descubre e instala nuevas versiones estables desde la aplicación |
| **Claves locales** | Conserva las claves API en el dispositivo y nunca las muestra completas |

<br />

<img src="assets/aidoit-workflow-intl.svg" alt="Los proveedores y modelos se conectan mediante AiDoIt con Codex, Claude y DeepSeek Harness" width="100%" />

## 📦 Descarga e instalación

### Windows 10/11 x64

La versión estable actual para Windows es **AiDoIt v0.0.9**. Descárgala únicamente desde [GitHub Releases](https://github.com/AiDoIt-Platform/AiDoIt/releases/latest).

| Paquete | Uso recomendado | Descarga |
|---|---|---|
| `AiDoIt_0.0.9_x64-setup.exe` | Instalador estándar recomendado para la mayoría de usuarios | [Descargar Setup EXE](https://github.com/AiDoIt-Platform/AiDoIt/releases/download/v0.0.9/AiDoIt_0.0.9_x64-setup.exe) |

> [!TIP]
> Para verificar sumas de comprobación, actualizar o instalar un MSI de forma silenciosa, consulta la [guía de instalación de Windows](HelpMd/Windows/Installation/README.md).

### macOS (Apple Silicon)

[Descargar AiDoIt v0.0.9 DMG](https://github.com/AiDoIt-Platform/AiDoIt/releases/download/v0.0.9/AiDoIt_0.0.9_aarch64.dmg)

Arrastra AiDoIt a Applications.

Esta compilación usa firma ad-hoc y no está notarizada por Apple. Al abrirla por primera vez, puede ser necesario hacer clic derecho y seleccionar Abrir.

### Ubuntu x64 / ARM64

Instala en un servidor Ubuntu con el script en línea y elige Codex, Claude Code o ambos:

```bash
curl -fsSL https://service.aidoit.pro/install | bash
```

Desinstala y restaura la configuración de usuario guardada antes de la instalación:

```bash
curl -fsSL https://service.aidoit.pro/uninstall | bash
```

> [!IMPORTANT]
> `curl | bash` ejecuta directamente un script remoto. Verifica antes el dominio y el origen y sigue la [guía visual de Ubuntu](HelpMd/Ubuntu/README.md).

## 🚀 Inicio rápido

### Windows

1. Instala e inicia AiDoIt y deja que detecte las herramientas y sesiones locales.
2. Abre **Integración con Codex**, **Integración con Claude Code** o **DeepSeek Harness**.
3. Añade un proveedor e introduce una Base URL y una clave API de confianza.
4. Obtén o añade modelos y ejecuta primero una prueba de disponibilidad.
5. Elige el proveedor y modelo predeterminados y activa la integración.
6. Desactiva la integración externa cuando quieras restaurar la configuración oficial anterior.

### Ubuntu

1. Inicia sesión con el usuario normal que ejecutará Codex o Claude Code.
2. Ejecuta el comando anterior y elige el acceso `sk` o `account`.
3. Selecciona `both`, `codex` o `claude` como destino.
4. Ejecuta `codex` o `claude` y usa `/model` para elegir y probar un modelo.

| Quiero… | Empezar aquí |
|---|---|
| Usar modelos de proveedores en Codex o ChatGPT | [Codex en Windows](HelpMd/Windows/Codex/README.md) |
| Usar modelos de proveedores en Claude Code o Claude Desktop | [Claude en Windows](HelpMd/Windows/Claude/README.md) |
| Configurar Codex o Claude Code en Ubuntu | [Instalación y uso en Ubuntu](HelpMd/Ubuntu/README.md) |

## 🧩 Funciones principales

<details open>
<summary><strong>Integración con Codex y ChatGPT</strong></summary>

- Detecta automáticamente Codex, ChatGPT, Codex CLI y el estado de inicio de sesión.
- Permite usar modelos oficiales y de proveedores externos en paralelo.
- Instala, selecciona e inicia Codex y prueba los modelos antes de activarlos.
- Si una aplicación está ocupada, permite cerrarla de forma normal o forzada antes de continuar.

</details>

<details>
<summary><strong>Integración con Claude Code y Claude Desktop</strong></summary>

- Detecta, instala e inicia Claude Code automáticamente.
- Detecta y abre Claude Desktop o permite elegir un instalador local.
- Mantiene proveedores, modelos y credenciales de Claude separados de Codex.
- Restaura la configuración y los modelos anteriores al desactivar la integración.

</details>

<details>
<summary><strong>Administración de DeepSeek Harness</strong></summary>

- Instala, inicia, detiene y abre DeepSeek Harness Web.
- Administra de forma independiente proveedores, credenciales, modelos y modelo predeterminado.
- Muestra la capacidad de contexto y razonamiento y ejecuta pruebas de respuesta reales.
- No modifica los agentes, herramientas, sesiones ni tareas existentes de Harness.
- Protege la configuración activa mientras Harness se ejecuta.

</details>

<details>
<summary><strong>Administración de proveedores y modelos</strong></summary>

- Añade varios proveedores con direcciones, claves, modelos y estados independientes.
- Obtén modelos del servicio automáticamente o mantén la lista de forma manual.
- Selecciona favoritos y valores predeterminados sin volver a escribir las credenciales.
- Cambia la interfaz entre chino e inglés; AiDoIt recuerda la selección.

</details>

## 📚 Documentación

| Plataforma | Guías |
|---|---|
| Windows | [Instalación y actualización](HelpMd/Windows/Installation/README.md) · [Codex](HelpMd/Windows/Codex/README.md) · [Claude](HelpMd/Windows/Claude/README.md) |
| macOS | [Codex](HelpMd/macOS/Codex/README.md) · [Claude](HelpMd/macOS/Claude/README.md) |
| Ubuntu | [Instalación, configuración y pruebas](HelpMd/Ubuntu/README.md) |

También puedes explorar el [Centro de ayuda de AiDoIt](HelpMd/README.md) por plataforma.

## 🔐 Seguridad y privacidad

- Las claves API y su configuración permanecen en tu dispositivo; la interfaz nunca muestra la clave completa.
- Las credenciales y configuraciones de Codex, Claude y Harness están aisladas.
- AiDoIt guarda el estado original antes de activar una integración y puede restaurarlo después.
- Oculta claves, nombres de usuario, rutas locales y endpoints antes de compartir incidencias, registros o capturas.

> [!IMPORTANT]
> AiDoIt administra la configuración y el enrutamiento locales. Las solicitudes enviadas a terceros siguen sujetas a sus políticas de privacidad, precios y condiciones. Usa solo proveedores de confianza.

## ❓ Preguntas frecuentes

<details>
<summary><strong>¿AiDoIt sobrescribe mi configuración oficial?</strong></summary>

AiDoIt conserva el estado original al activar una integración y puede restaurarlo al desactivarla. Codex, Claude y Harness se administran por separado.

</details>

<details>
<summary><strong>¿Por qué falla la detección o la prueba de un modelo?</strong></summary>

Comprueba la Base URL, la clave API, la conexión de red y que el proveedor admita el protocolo requerido. No publiques nunca una clave completa.

</details>

<details>
<summary><strong>¿Puedo configurar varios proveedores?</strong></summary>

Sí. Cada proveedor puede tener su propio endpoint, clave, catálogo de modelos y estado de activación.

</details>

## 💬 Contacto y comentarios

- Proyecto: [AiDoIt-Platform/AiDoIt](https://github.com/AiDoIt-Platform/AiDoIt)
- Problemas e ideas: [Crear un issue](https://github.com/AiDoIt-Platform/AiDoIt/issues/new)
- Versiones anteriores: [GitHub Releases](https://github.com/AiDoIt-Platform/AiDoIt/releases)
- Licencia: [GNU GPL v3](LICENSE)

<div align="center">

**AiDoIt — Integra cualquier modelo en tu flujo de desarrollo de IA con menos fricción.**

</div>

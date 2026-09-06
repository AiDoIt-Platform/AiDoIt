<div align="center">

<img src="assets/aidoit-readme-cover.png" alt="AiDoIt verbindet KI-Provider, Modelle und Coding-Tools" width="100%" />

<br />

[简体中文](README.md) · [English](README.en.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Deutsch](README.de.md) · [العربية](README.ar.md) · [Español](README.es.md)

<br />

[![Version](https://img.shields.io/badge/Release-v0.0.9-7c3aed?style=for-the-badge)](https://github.com/AiDoIt-Platform/AiDoIt/releases/latest)
[![Windows](https://img.shields.io/badge/Windows-10%20%7C%2011-0ea5e9?style=for-the-badge&logo=windows11&logoColor=white)](https://github.com/AiDoIt-Platform/AiDoIt/releases/latest)
[![Ubuntu](https://img.shields.io/badge/Ubuntu-x64%20%7C%20ARM64-e95420?style=for-the-badge&logo=ubuntu&logoColor=white)](HelpMd/Ubuntu/README.md)
[![Datenschutz](https://img.shields.io/badge/API_Keys-bleiben_lokal-10b981?style=for-the-badge)](#-sicherheit-und-datenschutz)
[![Lizenz](https://img.shields.io/badge/License-GPLv3-f59e0b?style=for-the-badge)](LICENSE)

### Eine App für deine KI-Coding-Tools und Modelle

AiDoIt unterstützt **Windows und Ubuntu x64 / ARM64**. Verwalte **Codex, ChatGPT, Claude Code, Claude Desktop und DeepSeek Harness** unter Windows, installiere Codex und Claude Code auf Ubuntu-Servern und wechsle zwischen offiziellen Konten und externen Modellen.

[Jetzt herunterladen](https://github.com/AiDoIt-Platform/AiDoIt/releases/latest) · [Schnellstart](#-schnellstart) · [Bildanleitungen](#-dokumentation) · [Problem melden](https://github.com/AiDoIt-Platform/AiDoIt/issues/new)

</div>

---

## ✨ Warum AiDoIt?

| Funktion | Dein Vorteil |
|---|---|
| **Windows + Ubuntu** | Windows 10/11 sowie Ubuntu-x64-/ARM64-Kommandozeilenumgebungen abdecken |
| **Eine zentrale Oberfläche** | Codex, Claude und DeepSeek Harness verwalten, ohne ständig Konfigurationsdateien zu bearbeiten |
| **Automatische Erkennung** | Installierte Desktop-Apps, CLIs, Anmeldestatus und lokale Laufzeitumgebungen erkennen |
| **Mehrere Provider und Modelle** | Provider, Zugangsdaten und Modellkataloge getrennt verwalten und Standards jederzeit wechseln |
| **Test vor Aktivierung** | Reale Verfügbarkeit und Antwortzeit eines Modells vor der Übernahme prüfen |
| **Getrennte Konfiguration** | Codex, Claude und Harness unabhängig verwalten, damit sich Einstellungen nicht beeinflussen |
| **Sichere Wiederherstellung** | Ursprünglichen Zustand sichern und beim Deaktivieren die offizielle Konfiguration wiederherstellen |
| **Updates in der App** | Ab `v0.0.7` spätere stabile Versionen direkt in der App finden und installieren |
| **Lokale Schlüssel** | Provider-API-Keys bleiben auf deinem Gerät und werden nie vollständig angezeigt |

<br />

<img src="assets/aidoit-workflow-intl.svg" alt="Provider und Modelle werden über AiDoIt mit Codex, Claude und DeepSeek Harness verbunden" width="100%" />

## 📦 Download und Installation

### Windows 10/11 x64

Die aktuelle stabile Windows-Version ist **AiDoIt v0.0.9**. Lade sie ausschließlich über [GitHub Releases](https://github.com/AiDoIt-Platform/AiDoIt/releases/latest) herunter.

| Paket | Empfohlener Einsatz | Download |
|---|---|---|
| `AiDoIt_0.0.9_x64-setup.exe` | Standardinstaller, empfohlen für die meisten Nutzer | [Setup EXE herunterladen](https://github.com/AiDoIt-Platform/AiDoIt/releases/download/v0.0.9/AiDoIt_0.0.9_x64-setup.exe) |

> [!TIP]
> Hinweise zu Prüfsummen, Upgrades und stiller MSI-Installation findest du in der [Windows-Installationsanleitung](HelpMd/Windows/Installation/README.md).

### macOS (Apple Silicon)

[AiDoIt v0.0.9 DMG herunterladen](https://github.com/AiDoIt-Platform/AiDoIt/releases/download/v0.0.9/AiDoIt_0.0.9_aarch64.dmg)

AiDoIt nach Applications ziehen.

Dieser Build ist ad-hoc signiert und nicht von Apple notarisiert. Beim ersten Start kann ein Rechtsklick und Öffnen erforderlich sein.

### Ubuntu x64 / ARM64

Installiere Codex, Claude Code oder beide auf einem Ubuntu-Server mit dem Online-Skript:

```bash
curl -fsSL https://service.aidoit.pro/install | bash
```

Die Online-Deinstallation stellt die vor der Installation gesicherte Benutzerkonfiguration wieder her:

```bash
curl -fsSL https://service.aidoit.pro/uninstall | bash
```

> [!IMPORTANT]
> `curl | bash` führt ein Remote-Skript direkt aus. Prüfe Domain und Quelle und folge der vollständigen [Ubuntu-Bildanleitung](HelpMd/Ubuntu/README.md).

## 🚀 Schnellstart

### Windows

1. Installiere und starte AiDoIt und lass lokale Tools sowie den Anmeldestatus erkennen.
2. Öffne **Codex-Integration**, **Claude-Code-Integration** oder **DeepSeek Harness**.
3. Füge einen Provider mit vertrauenswürdiger Base URL und API-Key hinzu.
4. Lade oder ergänze Modelle und führe zuerst einen Verfügbarkeitstest aus.
5. Wähle Standard-Provider und -Modell und aktiviere die Integration.
6. Deaktiviere die Drittanbieter-Integration bei Bedarf, um die vorherige offizielle Konfiguration wiederherzustellen.

### Ubuntu

1. Melde dich als regulärer Benutzer an, der Codex oder Claude Code ausführen soll.
2. Führe den obigen Befehl aus und wähle `sk` oder `account`.
3. Wähle `both`, `codex` oder `claude` als Ziel.
4. Starte `codex` oder `claude` und wähle sowie teste mit `/model` ein Modell.

| Ich möchte … | Hier beginnen |
|---|---|
| Provider-Modelle in Codex oder ChatGPT verwenden | [Codex unter Windows](HelpMd/Windows/Codex/README.md) |
| Provider-Modelle in Claude Code oder Claude Desktop verwenden | [Claude unter Windows](HelpMd/Windows/Claude/README.md) |
| Codex oder Claude Code unter Ubuntu einrichten | [Installation und Nutzung unter Ubuntu](HelpMd/Ubuntu/README.md) |

## 🧩 Kernfunktionen

<details open>
<summary><strong>Codex- und ChatGPT-Integration</strong></summary>

- Codex, ChatGPT, Codex CLI und aktuellen Anmeldestatus automatisch erkennen.
- Offizielle Modelle und Modelle externer Provider parallel verwenden.
- Codex installieren, auswählen und starten; Modelle vorher real testen.
- Bei belegten Apps zwischen normalem Beenden und erzwungenem Schließen wählen.

</details>

<details>
<summary><strong>Claude Code und Claude Desktop</strong></summary>

- Claude Code automatisch erkennen, installieren und starten.
- Claude Desktop erkennen und öffnen oder ein lokales Installationspaket auswählen.
- Provider, Modelle und Zugangsdaten getrennt von Codex verwalten.
- Vorherige Einstellungen und Modelle beim Deaktivieren wiederherstellen.

</details>

<details>
<summary><strong>DeepSeek-Harness-Verwaltung</strong></summary>

- DeepSeek Harness Web installieren, starten, stoppen und öffnen.
- Provider, Zugangsdaten, Modelle und Standardmodell unabhängig verwalten.
- Kontext- und Reasoning-Fähigkeiten anzeigen und echte Antworttests ausführen.
- Bestehende Agents, Tools, Sitzungen und Aufgaben in Harness unverändert lassen.
- Aktive Konfiguration während des Betriebs schützen.

</details>

<details>
<summary><strong>Provider- und Modellverwaltung</strong></summary>

- Mehrere Provider mit eigenen Endpunkten, Schlüsseln, Modellen und Zuständen hinzufügen.
- Modelle automatisch vom Upstream laden oder die Liste manuell pflegen.
- Favoriten und Standards festlegen, ohne Zugangsdaten erneut einzugeben.
- Oberfläche sofort zwischen Chinesisch und Englisch wechseln; AiDoIt merkt sich die Auswahl.

</details>

## 📚 Dokumentation

| Plattform | Anleitungen |
|---|---|
| Windows | [Installation und Upgrade](HelpMd/Windows/Installation/README.md) · [Codex](HelpMd/Windows/Codex/README.md) · [Claude](HelpMd/Windows/Claude/README.md) |
| macOS | [Codex](HelpMd/macOS/Codex/README.md) · [Claude](HelpMd/macOS/Claude/README.md) |
| Ubuntu | [Installieren, konfigurieren und testen](HelpMd/Ubuntu/README.md) |

Alternativ kannst du das [AiDoIt-Hilfecenter](HelpMd/README.md) nach Plattform durchsuchen.

## 🔐 Sicherheit und Datenschutz

- Provider-API-Keys und Einstellungen bleiben auf deinem Gerät; vollständige Schlüssel werden nie angezeigt.
- Zugangsdaten und Konfigurationen von Codex, Claude und Harness bleiben getrennt.
- AiDoIt sichert den ursprünglichen Zustand vor der Aktivierung und kann ihn später wiederherstellen.
- Entferne API-Keys, Benutzernamen, lokale Pfade und Service-Endpunkte aus Issues, Logs und Screenshots.

> [!IMPORTANT]
> AiDoIt verwaltet lokale Konfiguration und Routing. An Drittanbieter gesendete Anfragen unterliegen weiterhin deren Datenschutzrichtlinien, Preisen und Bedingungen. Verwende nur vertrauenswürdige Provider.

## ❓ Häufig gestellte Fragen

<details>
<summary><strong>Überschreibt AiDoIt meine offizielle Konfiguration?</strong></summary>

AiDoIt sichert den ursprünglichen Zustand beim Aktivieren und kann ihn beim Deaktivieren wiederherstellen. Codex, Claude und Harness werden unabhängig verwaltet.

</details>

<details>
<summary><strong>Warum schlägt die Modellerkennung oder der Test fehl?</strong></summary>

Prüfe Base URL, API-Key, Netzwerkverbindung und ob der Provider das benötigte Protokoll unterstützt. Veröffentliche niemals einen vollständigen Schlüssel.

</details>

<details>
<summary><strong>Kann ich mehrere Provider konfigurieren?</strong></summary>

Ja. Jeder Provider kann einen eigenen Endpunkt, Schlüssel, Modellkatalog und Aktivierungszustand besitzen.

</details>

## 💬 Kontakt und Feedback

- Projekt: [AiDoIt-Platform/AiDoIt](https://github.com/AiDoIt-Platform/AiDoIt)
- Probleme und Ideen: [Issue erstellen](https://github.com/AiDoIt-Platform/AiDoIt/issues/new)
- Ältere Versionen: [GitHub Releases](https://github.com/AiDoIt-Platform/AiDoIt/releases)
- Lizenz: [GNU GPL v3](LICENSE)

<div align="center">

**AiDoIt — Bringe jedes Modell mit weniger Aufwand in deinen KI-Entwicklungsworkflow.**

</div>

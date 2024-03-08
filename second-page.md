# GuardianV - Installation

> [GuardianV](https://guardianv.de/) AntiCheat, definieren Sie Ihr FiveM-Erlebnis neu.

## Downloading

### Retrieve your Copy of GuardianV

Download the latest Resource from the FiveM Keymaster [Keymaster-Assets](https://keymaster.fivem.net/assets?search=GuardianV)




### GitHub Pages

#### Hosting Site

To host this template on GitHub Pages do the following:  

1. Log into GitHub if you have not done so already
2. Tap the **Use this template** button in the upper-right of this GitHub Repository and choose **Create a new repository**
3. Enter a name for your new Repository and then tap the **Create repository** button
4. Once your new Repostitory is created go to **Settings**, then select **Pages** from the left-hand sidebar, and under **Branch** choose **main** and then tap the **Save** button
5. Wait a minute or two and refresh the same **Pages** page - once your site is ready a message will be displayed at the top of the screen along with a site link and a **Visit site** button

#### Editing Content

How about editing the content of your new Docsify site on GitHub Pages? View the Markdown page you want to edit (for example, **README.md**) and tap the **Pencil Icon**, then save any changes by tapping the green **Commit changes...** button. In just a few moments the Docsify site will be automatically updated to reflect those changes.

### Viewing Locally 
Run `npx serve .` (Node.js users) or `python -m http.server 8000` (Python users) in the repo folder to serve run locally.

## Docsify Documentation

To learn more about using Docsify, visit https://docsify.js.org.



GuardianV Dokumentation
Willkommen zur offiziellen Dokumentation von GuardianV, dem fortschrittlichen AntiCheat-System, das speziell für FiveM-Server entwickelt wurde. Mit GuardianV können Sie Ihr Spielerlebnis auf FiveM durch eine umfangreiche Palette von Sicherheits- und Überwachungsfunktionen neu definieren.

Einführung
GuardianV bietet eine umfassende Lösung für die Sicherheit Ihres FiveM-Servers, indem es eine Vielzahl von Betrugsversuchen und unerwünschten Verhaltensweisen erkennt und verhindert. Von der Überprüfung der Spielerintegrität bis hin zur Verhinderung von Cheat-Nutzung stellt GuardianV sicher, dass Ihr Server eine faire und sichere Umgebung für alle Spieler bietet.

Erste Schritte
Bevor Sie GuardianV auf Ihrem Server installieren, stellen Sie sicher, dass Sie die folgenden Anforderungen erfüllt haben:

Ein laufender FiveM-Server
Grundlegendes Verständnis der Serververwaltung und -konfiguration
Installation
Laden Sie die neueste Version von GuardianV von der offiziellen Website oder unserem GitHub-Repository herunter.
Extrahieren Sie das heruntergeladene Paket in den resources Ordner Ihres FiveM-Servers.
Fügen Sie ensure GuardianV zu Ihrer server.cfg Datei hinzu, um das Script zu starten.
Konfiguration
Nach der Installation müssen Sie die Konfigurationsdatei config.lua an Ihre Serverbedürfnisse anpassen. Im Folgenden finden Sie eine Übersicht über einige der wichtigsten Konfigurationsoptionen:

lua
Copy code
GUARDIANV.ApiKey = "Ihr-API-Schlüssel-hier"
GUARDIANV.Username = "Ihr-Username-hier"

-- Servereinstellungen
GUARDIANV.ServerConfig = {
    Name = "Ihr Servername hier",
    Port  = "30120"
}

-- Chat-Einstellungen
GUARDIANV.ChatSettings = {
    Enable      = true,
    PrivateWarn = true,
}

-- Und so weiter für jede Konfigurationsoption...
Wichtige Konfigurationsoptionen
ApiKey: Ihr persönlicher API-Schlüssel für GuardianV.
Username: Ihr Benutzername.
ServerConfig: Grundlegende Serverinformationen wie Name und Port.
ChatSettings: Einstellungen bezüglich des Chats auf Ihrem Server.
Für eine detaillierte Beschreibung aller Konfigurationsoptionen besuchen Sie bitte unsere Konfigurationsdokumentation.

Funktionen
GuardianV kommt mit einer Reihe von Funktionen, um die Sicherheit Ihres Servers zu gewährleisten. Einige der Hauptfunktionen sind:

Anti-Cheat Erkennung: Erkennt und verhindert eine Vielzahl von Cheats und Hacks.
Anpassbare Strafen: Konfigurieren Sie individuelle Strafen für unterschiedliche Verstöße.
Erweiterte Protokollierung: Detaillierte Protokolle von Spieleraktionen und Systemereignissen.
Serverüberwachung: Überwachen Sie die Leistung und Stabilität Ihres Servers in Echtzeit.
Unterstützung
Wenn Sie Hilfe benötigen oder Fragen zur Konfiguration und Nutzung von GuardianV haben, besuchen Sie bitte unser Support-Forum oder kontaktieren Sie uns direkt über unsere Website.
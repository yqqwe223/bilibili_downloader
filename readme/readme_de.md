# 🎬 Bilibili Video-Analyse-Tool

> Ein leichtes, schnelles und vielseitiges Werkzeug zum Extrahieren von Videoinhalten von Bilibili (Lern- & Forschungsversion)

[🌐 Online-Demo](https://twittervideodownloaderx.com/bilibili_downloader_ge) • [📝 Bedienungsanleitung](#-bedienungsanleitung) • [❓ Häufig gestellte Fragen](#-häufig-gestellte-fragen)

---

## 📋 Projektübersicht

Dieses Projekt ist ein webbasiertes Video-Analyse-Tool, das darauf ausgelegt ist, Metadaten von Medienressourcen aus öffentlichen Videos auf der Bilibili-Plattform (哔哩哔哩) sicher zu extrahieren und Optionen für Formatkonvertierung sowie lokales Speichern bereitzustellen. Keine Installation von Client-Software oder Konto-Registrierung erforderlich – nutzen Sie das Tool direkt über Ihren Browser.

> ⚠️ **Wichtiger Hinweis**: Dieses Tool dient ausschließlich persönlichen Lernzwecken, technischer Forschung und der Nutzung im Rahmen einer angemessenen Verwendung. Bitte halten Sie sich an die [Bilibili-Community-Richtlinien](https://www.bilibili.com/blackboard/protocol.html), das 《Urheberrechtsgesetz der Volksrepublik China》 sowie andere geltende Vorschriften. Respektieren Sie die Arbeit der Kreativschaffenden; verwenden Sie heruntergeladene Inhalte nicht für kommerzielle Zwecke oder zur Verletzung von Rechten Dritter.

---

## ✨ Hauptfunktionen

- 🔗 **Link-Analyse**: Unterstützt standardmäßige Bilibili-Video/Anime-URLs; automatische Erkennung von Episoden und verfügbaren Auflösungs-Optionen
- 📥 **Export in mehreren Formaten**:
  - Originaler Video-Stream (unterstützt öffentliche Auflösungen wie 1080P/720P usw.)
  - Audio-Extraktion → MP3-Format (praktisch für das Offline-Hören von Vorträgen/Musik)
  - Videoclip → Konvertierung zu animiertem GIF (ideal für Memes/Lehrdemonstrationen)
- 🌍 **Mehrsprachige Oberfläche**: Unterstützung für Deutsch, Englisch, Chinesisch, Japanisch, Koreanisch und weitere Sprachen
- 📱 **Plattformübergreifende Kompatibilität**: Funktioniert einwandfrei auf Chrome / Firefox / Safari / Edge; optimierte Erfahrung für Mobilgeräte und Tablets
- 🔒 **Datenschutz priorisiert**: Keine Bilibili-Konto-Anmeldung erforderlich, keine Erfassung personenbezogener Daten; Analyseprozess vollständig anonym
- ⚡ **Schnelle Verarbeitung**: Analyse im Durchschnitt in 5-10 Sekunden abgeschlossen; Unterstützung für parallele Anfragen und Stapelverarbeitung

---

## 🚀 Schnellstart

### Online-Nutzung (empfohlen)
1. Besuchen Sie [https://twittervideodownloaderx.com/bilibili_downloader_ge](https://twittervideodownloaderx.com/bilibili_downloader_ge)
2. Kopieren Sie den Link des Zielvideos (Beispiel: `https://www.bilibili.com/video/BV1xx411c7mD`)
3. Fügen Sie den Link in das Eingabefeld ein → Klicken Sie auf die Schaltfläche 「Analysieren」
4. Wählen Sie die gewünschte Auflösung und das Format → Speichern Sie die Datei gemäß den Anweisungen Ihres Browsers

### Lokale Bereitstellung (für Entwickler)
```bash
# Repository klonen
git clone https://github.com/your-repo/bili-video-parser.git

# Abhängigkeiten installieren
cd bili-video-parser && npm install

# Umgebungsvariablen konfigurieren (optional)
cp .env.example .env

# Entwicklungsserver starten
npm run dev
```

> 💡 Hinweis: Dieses Projekt verwendet eine Architektur basierend auf Node.js + Express. Detaillierte Bereitstellungsinformationen finden Sie in `/docs/DEPLOY.md`

---

## 🛠 Technologie-Stack

| Modul | Eingesetzte Technologien |
|-------|--------------------------|
| Frontend | Vue 3 + TypeScript + Vite |
| Backend | Node.js + Express + Axios |
| Videoverarbeitung | ffmpeg.wasm (leichtgewichtige Client-seitige Konvertierung) |
| Proxy-Weiterleitung | Cloudflare Workers / Benutzerdefinierte Middleware |
| Internationalisierung | vue-i18n + JSON-Sprachpakete |

---

## 📚 Bedienungsanleitung

### Grundlegender Arbeitsablauf
```
1. Video-Link erhalten
   └─ Öffnen Sie das Zielvideo auf Bilibili → Kopieren Sie die URL aus der Adressleiste des Browsers

2. Analyse-Anfrage senden
   └─ Fügen Sie den Link in das Eingabefeld des Tools ein → Klicken Sie auf 「Analyse starten」

3. Ausgabe-Konfiguration auswählen
   ├─ 🎬 Video herunterladen: Auflösung wählen (360P/720P/1080P usw. - nur öffentliche Optionen)
   ├─ 🎵 Audio extrahieren: MP3-Datei generieren (ideal für Offline-Hören von Vorträgen/Musik)
   └─ 🎞 GIF generieren: Animation aus angegebenem Zeitbereich erstellen (empfohlen: ≤15 Sekunden)

4. Datei speichern
   └─ Die Ressource wird in einem neuen Tab geöffnet → Rechtsklick/Menü → 「Speichern unter」
```

### Tipps für die Nutzung auf Mobilgeräten
- iOS Safari: Schaltfläche „Teilen" → 「In Dateien speichern」
- Android Chrome: Video-Vorschau lange drücken → 「Video herunterladen」
- Bei automatischer Wiedergabe: Klicken Sie auf `⋮` oben rechts im Player → Wählen Sie 「Herunterladen」

---

## ❓ Häufig gestellte Fragen

**F: Wo werden heruntergeladene Dateien gespeichert?**  
A: Dateien werden im im Browser konfigurierten Download-Ordner gespeichert. Sie können diesen Pfad in den Browsereinstellungen überprüfen oder ändern.

**F: Kann ich Inhalte für Mitglieder oder anmeldepflichtige Inhalte analysieren?**  
A: Nein. Dieses Tool funktioniert nur mit Videos, die als öffentlich eingestellt sind, und respektiert die Zugriffseinstellungen des Originalinhalts.

**F: Wird die Bild-/Tonqualität nach der Konvertierung reduziert?**  
A: Video-Downloads behalten die originale Bitrate der ausgewählten Auflösung bei. Das MP3-Format verwendet eine Standardkodierung mit 128 kbps. Das GIF-Format optimiert die Bildrate entsprechend der Dauer, um ein Gleichgewicht zwischen Dateigröße und Flüssigkeit zu erreichen.

**F: Wird der Download-Verlauf oder Cache gespeichert?**  
A: Nein. Alle Ressourcen werden direkt über einen temporären Proxy an das Gerät des Nutzers übertragen; der Server speichert keine Anfragen oder Mediendateien.

**F: Was tun, wenn die Analyse fehlschlägt?**  
A: Bitte überprüfen Sie: ① Ob der Link zu einem gültigen öffentlichen Video führt ② Ob Ihre Internetverbindung stabil ist ③ Versuchen Sie es mit einem anderen Browser. Bei fortbestehenden Problemen melden Sie dies bitte über ein Issue.

---

## ⚖️ Einhaltung von Vorschriften und Haftungsausschluss

- Dieses Tool **umgeht oder verletzt keine technischen Schutzmaßnahmen** der Plattform; es ruft lediglich Metadaten über öffentliche Schnittstellen ab
- Der Nutzer ist selbst dafür verantwortlich, sicherzustellen, dass seine Nutzung den örtlichen Gesetzen und den Nutzungsbedingungen der Plattform entspricht
- Empfohlene Anwendungsfälle: Persönliche Lernarchivierung, Bildungspräsentationen, Referenzmaterial für die Inhaltserstellung... stets im Rahmen der zulässigen Nutzung (Fair Use)
- Wenn Sie Inhalte entdecken, die möglicherweise Rechte verletzen, wenden Sie sich bitte über [das Urheberrechts-Meldeformular von Bilibili](https://www.bilibili.com/blackboard/help.html#copyright) an den offiziellen Kanal

---

## 🤝 Leitfaden für Beiträge

Wir freuen uns über Ihre Pull Requests und Issue-Meldungen! Vor dem Beitragen bitten wir Sie, Folgendes zu lesen:
- [Code-Standards](/CONTRIBUTING.md)
- [Mehrsprachiger Übersetzungsleitfaden](/locales/README.md)
- [Sicherheits- und Compliance-Anforderungen](/SECURITY.md)

---

## 📄 Lizenz

Dieses Projekt wird unter der [MIT-Lizenz](/LICENSE) veröffentlicht. Es kann kostenlos für Bildungs- und Forschungszwecke genutzt werden. Bei kommerzieller Nutzung prüfen Sie bitte sorgfältig die Einhaltung der geltenden rechtlichen Vorschriften.

---

> 🌟 Wenn Ihnen dieses Tool hilfreich war, würden wir uns sehr über ✨einen Stern (Star) freuen! Ihre Unterstützung ist die größte Motivation für uns, dieses Projekt weiterhin zu pflegen und zu verbessern~

*Zuletzt aktualisiert: Mai 2026 | Version: v1.0.0*
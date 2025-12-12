# KI-Begriffe und ihre Zusammenhänge (für Office-Nutzer)

Als Office-Anwender wirkt KI oft wie Magie, aber es ist wie eine gut organisierte Abteilung. Hier ist die Logik dahinter:

## 1. Das kleine Lexikon (Definitionen)

* **Modell (LLM):** Das "Gehirn". Ein statisches Programm, das Text vorhersagt (z.B. GPT-4, Gemini 1.5, Claude 3.5). Es weiß nur das, was es im Training gelernt hat.
* **Agent:** Der "Mitarbeiter". Ein System, das das Modell nutzt, um Aufgaben zu verstehen und *aktiv* auszuführen.
* **Extensions (Gemini) / Connectors (Claude):** Die "Hände" oder "Werkzeuge". Sie verbinden den Agenten mit externen Diensten (z.B. E-Mails, Kalender).
* **RAG (Retrieval Augmented Generation):** Die "Methode". Der Prozess, bei dem der Agent erst in Dokumenten "nachschlägt" (Retrieval) und diese Info für die Antwort nutzt.
* **MCP Server:** Der "Universal-Stecker". Ein Standard, damit Agenten sicher auf lokale Daten oder Firmen-Datenbanken zugreifen können.
* **Gems (Gemini) / Projekte (Claude):** Die "Persona". Eine gespeicherte Konfiguration, die dem Agenten sagt, wer er ist und was er darf.

---

## 2. Die Zusammenhänge (Wer macht was mit wem?)

Denk daran: **Der Agent ist der Akteur**, der Rest ist Zubehör oder Gehirnmasse.

### Modell & Agent (Gehirn & Körper)
* **Ein Agent nutzt ein Modell zum Denken.** Ohne Modell ist der Agent leblos.
* **Viele Agenten können dasselbe Modell nutzen.** Mehrere "Gems" greifen im Hintergrund auf dasselbe "Gehirn" (z.B. Gemini Pro) zu.
* **Das Modell liefert das Vokabular, der Agent liefert die Ausführung.**

### Extensions & RAG (Werkzeuge & Arbeitsweise)
* **Extensions sind oft die Voraussetzung für RAG.** Um in E-Mails nachzuschlagen, braucht der Agent die "Hände" (Extension), um die Mails zu greifen.
* **Der Agent nutzt Extensions gegen "Blindheit".** Das Modell kennt deine Termine nicht. Der Agent nutzt die Extension, um in den Kalender zu schauen.
* **RAG ist das "Lesen vor dem Schreiben".** Wenn der Agent eine PDF durchsucht, betreibt er RAG.

### MCP Server (Die Verbindung)
* **Ein MCP Server ist eine standardisierte Extension.** Er dient als Universal-Adapter für Datenbanken.
* **MCP ermöglicht RAG auf eigenen Daten.** Du startest einen MCP Server, damit der Agent deine lokale Dateiablage "lesen" darf.

### Gems / Projekte (Die Konfiguration)
* **Ein Gem/Projekt ist ein "vorkonfigurierter" Agent.** Es ist wie eine gespeicherte Stellenbeschreibung.
* **Gems nutzen RAG automatisch.** Wenn du eine Datei in ein Projekt lädst, nutzt der Agent RAG, um Antworten nur aus diesem Wissen zu generieren.

---

## 3. Die Büro-Analogie

| KI-Begriff | Entspricht im Büro | Erklärung |
| :--- | :--- | :--- |
| **Modell** | **IQ / Abschluss** | Das Grundwissen und die Sprachfähigkeit. |
| **Agent** | **Mitarbeiter** | Die Person, die die Aufgabe erledigt. |
| **Gem/Projekt** | **Stellenprofil** | Die Anweisung: "Du bist jetzt Buchhalter." |
| **Extension/MCP** | **Archivschlüssel** | Der Zugang zu den Aktenschränken (Daten). |
| **RAG** | **Nachschlagen** | Die Tätigkeit, eine Akte zu holen und zu lesen. |

# Was ist denn nun "Der Agent"?

Der Begriff ist abstrakt. Hier ist die konkrete Einordnung für den Alltag:

## Die Hierarchie

1.  **Die Plattform (Gemini App / Claude.ai):**
    Das ist das **Bürogebäude**. Es stellt die Infrastruktur bereit (Login, Chat-Fenster, Server), aber es "denkt" nicht selbst.

2.  **Das Gem / Projekt:**
    Das ist die **Stellenbeschreibung**. Hier steht geschrieben: "Du bist ein Reisekosten-Experte und kennst die PDF 'Reiserichtlinie'." Es ist aber nur eine "ruhende" Datei.

3.  **Der Agent (Die aktive Instanz):**
    Sobald Sie einen **neuen Chat starten** (egal ob mit dem Standard-Bot oder einem speziellen Gem), interagieren Sie mit dem **Agenten**.

---

## Der Lackmustest: Chatbot vs. Agent

Wie unterscheiden Sie, ob Sie nur mit einem Textgenerator oder einem echten Agenten sprechen?

* **Der reine Chatbot (Das Modell):**
    * *Sie:* "Was ist die Hauptstadt von Frankreich?"
    * *KI:* "Paris."
    * *Erklärung:* Die KI nutzt nur ihr internes Wissen. Sie **redet** nur.

* **Der Agent (Das handelnde System):**
    * *Sie:* "Such mir ein Hotel in Paris und speichere es in meiner Reiseliste."
    * *KI:* "Ich habe Hotel X gefunden und es via Google Maps Extension gespeichert."
    * *Erklärung:* Die KI nutzt **Extensions/Werkzeuge**. Sie **handelt** aktiv in Ihrer Welt.

> **Merksatz für Office-Nutzer:**
> Das **Gem** definiert die Rolle, das **Modell** liefert die Intelligenz, und sobald das System anfängt, Werkzeuge (Extensions) zu benutzen, nennen wir es einen **Agenten**.
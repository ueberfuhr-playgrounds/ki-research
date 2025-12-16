## MCP Architektur-Konzepte: Eine Einführung

### 1. Die Grundidee: Die Brücke
Stellt euch vor, wir haben ein altes System (z.B. eine Kundenverwaltung), das nur über eine klassische technische Schnittstelle (REST API) erreichbar ist. Der **KI-Agent** (z.B. Claude Desktop oder eine IDE) weiß zunächst nicht, wie er diese bedienen soll.
Hier kommt der **MCP-Server** ins Spiel. Er dient als Dolmetscher (Bridge).

* **KI-Agent (Client):** "Ich möchte Herrn Müller grüßen."
* **MCP-Server (Bridge):** Übersetzt das in einen technischen Befehl für das alte System.
* **Backend (REST API):** Führt den Befehl aus.

### 2. Die zwei Wege der Kommunikation

Wir unterscheiden zwei Hauptarten, wie der KI-Agent mit diesem Dolmetscher sprechen kann.

#### A. Der lokale Weg (Local Subprocess / STDIO)
Das ist wie ein Gespräch im selben Raum.
* **Wo läuft es?** Der MCP-Server läuft direkt auf **deinem Computer**, unsichtbar im Hintergrund.
* **Wie kommunizieren sie?** Über direkte Textnachrichten (wir nennen das "Standard Input/Output" oder STDIO). Das Format ist JSON-RPC (strukturierte Notizzettel).
* **Vorteil:** Sehr schnell, sicher (da nichts das Haus verlässt), einfach einzurichten.

#### B. Der ferne Weg (Remote / HTTP & SSE)
Das ist wie ein Telefonat mit einer Zentrale.
* **Wo läuft es?** Der MCP-Server läuft auf einem **Server** im Rechenzentrum oder in der Cloud.
* **Wie kommunizieren sie?** Über das Internet. Da der KI-Agent manchmal warten muss, bis der Server antwortet, nutzen wir eine dauerhafte Leitung (Server-Sent Events / SSE), damit der Server Statusmeldungen "streamen" kann, ohne dass wir ständig nachfragen müssen ("Sind wir schon da?").
* **Vorteil:** Zentral verwaltet, alle Mitarbeiter nutzen den gleichen Stand, Updates müssen nicht auf jedem PC installiert werden.

### 3. Der Ablauf: In 3 Schritten zum Ziel (Das "HalloWelt"-Beispiel)

Egal ob lokal oder remote, der Tanz ist immer der gleiche:

1.  **Phase 1: Der Handshake (Initialisierung)**
    * *KI-Agent:* "Hallo, ich spreche MCP Version 1. Was sprichst du?"
    * *MCP-Server:* "Hallo! Ich spreche auch Version 1. Ich bin bereit."
    
2.  **Phase 2: Die Speisekarte (List Tools)**
    * *KI-Agent:* "Was hast du für Werkzeuge (Tools) im Angebot?"
    * *MCP-Server:* "Ich habe ein Tool namens `say_hello`. Das braucht einen Namen als Eingabe."

3.  **Phase 3: Die Bestellung (Call Tool)**
    * *KI-Agent:* "Super. Führe bitte `say_hello` aus mit dem Namen 'Max'."
    * *MCP-Server (intern):* Ruft jetzt das echte Backend (REST API) auf.
    * *MCP-Server:* "Hier ist das Ergebnis: 'Hallo Max, willkommen im System!'."

### 4. Sicherheit: Wer darf was? (OAuth Flows)

Wenn der MCP-Server auf Daten zugreifen will, muss er wissen, ob er das darf. Je nach Architektur bieten sich unterschiedliche Verfahren an.

| Szenario | Authentifizierungsmethode | Erklärung |
| :--- | :--- | :--- |
| **Lokal** | **API-Keys (Umgebungsvariablen)** | *Der einfache Weg:* Der Schlüssel liegt bereits auf deinem PC (z.B. in einer `.env` Datei). Der Server liest ihn beim Start einfach aus. |
| **Lokal** | **OAuth Device Flow** | *Der interaktive Weg:* Ideal für lokale Tools ohne eigene grafische Oberfläche. Der Server gibt einen Code und eine URL aus (wie beim Login am Smart-TV). Du bestätigst den Code im Browser, und der Server erhält im Hintergrund die Erlaubnis. |
| **Remote** | **OAuth Authorization Code Flow** | *Der klassische Web-Weg:* Der Prozess startet im Browser. Du wirst zum Anbieter (z.B. Google/Microsoft) umgeleitet, loggst dich ein, und wirst mit einem Ticket zurück zum Server geleitet. |

---

### Vergleich der Ansätze

| Merkmal | Lokal (STDIO) | Remote (HTTP/SSE) |
| :--- | :--- | :--- |
| **Ort der Ausführung** | Dein Laptop / PC | Server / Cloud |
| **Verbindung** | Direktes Rohr (Pipe) | Netzwerk / Internet |
| **Komplexität** | Gering (Starten & Loslegen) | Höher (Netzwerk, Firewalls) |
| **Datenschutz** | Daten bleiben oft lokal | Daten verlassen das Gerät |
| **Einsatzgebiet** | Persönliche Tools, Dateien bearbeiten | Firmenweite Tools, Zugriff auf zentrale DB |
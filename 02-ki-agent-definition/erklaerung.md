# Trainingskonzept: Vom LLM zum KI-Agenten

Das Ziel ist es, das „Aha-Erlebnis“ zu erzeugen: *„Ach, die KI kann das auch für mich **ausführen**?“*

Hier ist das Konzept, strukturiert in vier logische Phasen.

---

### Phase 1: Die Brücke bauen – Das "Gehirn im Glas"
Zuerst müssen wir das Vorwissen (LLM) abholen und dessen Limitierung aufzeigen.

**Die Erklärung:**
> „Erinnert euch an das LLM (Large Language Model), das wir kennengelernt haben. Stellt euch das LLM wie ein **super-intelligentes Gehirn in einem Glas** vor.
> * Es hat alle Bücher der Welt gelesen.
> * Es kann Gedichte schreiben, komplexe Texte analysieren und Witze erzählen.
> * **Aber:** Es hat keine Hände. Es hat keine Augen für das, was *jetzt gerade* passiert. Es kann nicht in euren Kalender schauen und es kann keine E-Mail abschicken. Es ist im Glas gefangen.“

**Das Problem:**
Wenn ihr das "Gehirn" fragt: *„Habe ich morgen Zeit für ein Meeting?“*, wird es antworten: *„Ich bin eine KI, ich kenne deinen Kalender nicht.“*

---

### Phase 2: Die Definition – Was ist ein KI-Agent?
Jetzt führen wir den Agenten als die Lösung für dieses Problem ein.

**Die Formel:**
$$\text{LLM (Wissen)} + \text{Werkzeuge (Zugriff)} = \text{KI-Agent}$$

**Die Analogie:**
> „Ein KI-Agent ist dieses Gehirn, dem wir nun **Arme, Beine und einen Laptop** geben.
> * Wir geben ihm Zugriff auf E-Mails.
> * Wir geben ihm die Erlaubnis, in Datenbanken zu lesen.
> * Wir erlauben ihm, Knöpfe zu drücken (z.B. 'Senden').
>
> Der Agent **denkt** mit dem LLM, aber er **handelt** mit seinen Werkzeugen.“

---

### Phase 3: Der Gamechanger – Integration externer Systeme
Wir adressieren das Problem des **„Kontext-Wechsels“** (Context Switching).

**Das Szenario (Ohne Agent):**
1.  Ihr lest eine Kunden-E-Mail (Outlook).
2.  Ihr sucht Informationen dazu im Firmen-Wiki (Confluence).
3.  Ihr erstellt ein Ticket für die IT (Jira).
4.  Ihr schreibt dem Kollegen ein Update (Teams).
* *Fazit:* 4 Fenster offen, viel Copy-Paste, hohe Fehleranfälligkeit.

**Das Szenario (Mit KI-Agent):**
Ihr sagt dem Agenten nur einen Satz:
> *„Der Kunde Müller meldet Fehler X. Bitte recherchiere die Lösung im Wiki, erstell ein Jira-Ticket für das Tech-Team und gib Peter in Teams kurz Bescheid.“*

**Was passiert im Hintergrund?**
1.  **Denken:** Der Agent analysiert den Satz (LLM).
2.  **Planen:** Er merkt: „Ich brauche Infos aus Confluence.“ $\rightarrow$ *Führt Suche aus.*
3.  **Handeln:** Er merkt: „Ich muss ein Ticket erstellen.“ $\rightarrow$ *Nutzt die Jira-Schnittstelle.*
4.  **Kommunizieren:** Er merkt: „Peter informieren.“ $\rightarrow$ *Schreibt in Teams.*

---

### Phase 4: Warum ist das effizienter? (Takeaways)

| Merkmal | LLM (ChatGPT pur) | KI-Agent (im Firmennetz) |
| :--- | :--- | :--- |
| **Wissen** | Stand von gestern (Trainingsdaten) | Echtzeit-Wissen (Live-Daten) |
| **Zugriff** | Öffentlich verfügbarer Text | Interne Dokumente (Confluence, SharePoint) |
| **Aktion** | Gibt nur Text aus | Führt Aktionen aus (Buchen, Senden, Erstellen) |
| **Rolle** | Ein Lexikon | Ein digitaler Mitarbeiter |

**Wichtige Botschaft:**
> „KI-Agenten befreien euch von der 'Copy-Paste-Bürokratie'. Ihr seid nicht mehr die Schnittstelle zwischen den Programmen – der Agent übernimmt das.“
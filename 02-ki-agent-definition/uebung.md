# Schulungsmodul: Die Evolution der Arbeit – Von ChatGPT zum KI-Agenten

**Lernziel:** Verstehen, wie KI-Agenten durch System-Integration und "Gedächtnis" den Arbeitsaufwand im Vergleich zu reinen LLMs drastisch reduzieren.

---

## Das Szenario
Ein Kunde schreibt eine E-Mail: *„Wo bleibt meine Bestellung #123?“*
Wir vergleichen drei Wege, diese Aufgabe zu lösen.

---

### Stufe 1: Der manuelle Weg (Ohne KI)
*Der Mensch macht alles selbst. Er ist der Arbeiter.*

**Der Ablauf:**
1.  **Lesen:** Ich lese die E-Mail.
2.  **Recherche:** Ich wechsele das Fenster zum ERP-System, suche nach `#123` und merke mir: *"Status ist Versandt"*.
3.  **Schreiben:** Ich öffne Outlook und tippe mühsam selbst: *"Sehr geehrter Herr Müller, vielen Dank für..."*
4.  **Abschluss:** Senden.

* **Nachteil:** Hoher Zeitaufwand, Medienbrüche, repetitive Tipparbeit.

---

### Stufe 2: Der Weg mit LLM / ChatGPT (Der "Daten-Kurier")
*Der Mensch nutzt KI zum Texten, muss ihr aber die Welt erklären. Er ist die Schnittstelle.*

**Der Ablauf:**
1.  **Recherche (Mensch):** Ich muss **zuerst** ins System schauen. Ich finde heraus: *"Status ist Versandt"*.
2.  **Prompting (Mensch):** Ich gehe zu ChatGPT. Damit das Ergebnis gut wird, muss ich einen **umfangreichen Prompt** schreiben (die 4 Kriterien):
    * **Rolle:** *"Du bist ein professioneller Support-Mitarbeiter."*
    * **Kontext/Daten:** *"Der Kunde fragt nach #123. Ich habe nachgesehen: Sie ist versandt."* (Das muss ich manuell eingeben!)
    * **Aufgabe:** *"Schreibe eine Antwort-Mail."*
    * **Format:** *"Sei sehr höflich, nutze 'Sie' und halte dich kurz."*
3.  **Generierung (KI):** Das LLM schreibt den Text.
4.  **Transfer (Mensch):** Ich kopiere den Text $\rightarrow$ wechsele zu Outlook $\rightarrow$ füge ein $\rightarrow$ Senden.

* **Das Problem:** Ich muss mich ständig wiederholen (Rolle/Format immer neu eingeben) und Daten manuell von A nach B tragen.

---

### Stufe 3: Der Weg mit KI-Agent (Der "eingearbeitete Kollege")
*Der Agent hat Zugriff auf Tools und kennt seinen Job. Der Mensch ist der Manager.*

**Vorbereitung (Einmalig im Hintergrund):**
Der Agent wurde "eingestellt" (programmiert). In seinem **System Prompt** (seiner Jobbeschreibung) steht fest verankert:
> *"Du bist der Support-Bot. Deine Tonalität ist immer höflich und per 'Sie'. Wenn Daten fehlen, nutze das ERP-Tool."*

**Der tägliche Ablauf (User):**
1.  **Delegation (Mensch):** Ich gebe nur noch einen **kurzen Befehl**:
    > *"Kümmer dich um Bestellung #123."*
2.  **Ausführung (Agent):**
    * **Erinnert sich:** *"Aha, ich bin Support (Rolle), ich muss höflich sein (Format)."* (Muss der User nicht mehr sagen).
    * **Handelt:** Der Agent loggt sich selbst ins System ein, sieht *"Versandt"*.
    * **Schreibt:** Erstellt die Mail im Firmen-Design.
    * **Liefert:** Legt den Entwurf in Outlook ab oder sendet direkt.

* **Der Gewinn:** Der User spart sich das "Briefing" (Rolle/Format) und die "Recherche" (Daten). Maximale Effizienz.

---

## Die Analogie zum Merken

Um den Unterschied zwischen Stufe 2 und 3 zu verstehen:

| Merkmal | LLM (ChatGPT Session) | KI-Agent (Integriert) |
| :--- | :--- | :--- |
| **Vergleich** | **Der Freelancer** | **Der Festangestellte** |
| **Wissen** | Kommt neu rein, kennt die Firma nicht. | Wurde "onboarded", kennt die Prozesse. |
| **Anweisung** | Ich muss jedes Mal alles erklären: *"Sei nett, wir sind Firma X, hier sind die Daten..."* | Weiß Bescheid. Braucht nur das Ziel: *"Mach das fertig."* |
| **Zugriff** | Hat keine Schlüssel (Tools). | Hat einen Schlüssel zum Büro (Login für Jira/Teams). |

---

## Fazit für die Praxis
* **LLMs** sind großartige **Texter**, brauchen aber viel Führung (Prompting).
* **Agenten** sind digitale **Mitarbeiter**, die Aufgaben autonom über Systemgrenzen hinweg erledigen.
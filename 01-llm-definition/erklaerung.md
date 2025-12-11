# Schulungsmaterial: KI-Grundlagen für Sachbearbeiter

## Einführung: Was ist ein Large Language Model (LLM)?

Wir verzichten auf komplexe Mathematik und nutzen drei einfache Analogien, um zu verstehen, wie KI-Modelle wie ChatGPT funktionieren.

### 1. Der Aufbau: Die riesige Bibliothek
Stellen Sie sich das KI-Modell nicht als Computer vor, der "denkt", sondern als eine gigantische Bibliothek.
* **Large (Groß):** Das Modell wurde mit fast allem Text aus dem Internet gefüttert (Bücher, Wikipedia, Artikel).
* **Language Model (Sprachmodell):** Es speichert keine Fakten wie eine Datenbank, sondern analysiert Muster.
* **Analogie:** Wie ein Kollege, der die echte Welt nie gesehen hat, aber jedes Buch darüber gelesen hat. Er weiß nicht, wie sich Regen anfühlt, aber er weiß genau, welche Wörter (nass, kalt, Schirm) statistisch dazu gehören.

### 2. Das Lernen: Der ewige Lückentext
Wie lernt der Computer Sprache? Durch Milliarden von Lückentexten.
1. **Das Training:** Der Computer bekommt den Satz "Der Hund jagt die ...".
2. **Der Rat:** Er rät ein Wort. Ist es falsch, korrigieren wir ihn.
3. **Das Ergebnis:** Er passt seine internen Wahrscheinlichkeiten an. Irgendwann weiß er: Auf "Hund jagt" folgt oft "Katze", aber fast nie "Bratpfanne".

### 3. Die Generierung: Die ultimative Autovervollständigung
Wenn die KI antwortet, "denkt" sie nicht über eine Antwort nach. Sie sagt immer nur das **nächste Wort** voraus (ähnlich wie beim Smartphone, nur viel klüger).
* Sie reiht Wort für Wort aneinander, basierend darauf, was statistisch am besten passt.
* Deshalb kann sie Stile imitieren, aber keine Fakten garantieren.

> **⚠️ Wichtige Warnung: Halluzinationen**
> Da das Modell immer nur das *wahrscheinlichste* Wort sucht, kann es Fakten erfinden (Halluzinieren). Wenn es ein Aktenzeichen nicht kennt, erfindet es eines, das *echt aussieht*.
> **Merke:** Ein LLM ist ein Meister der Sprache, aber kein Meister der Wahrheit. Immer Fakten prüfen!

---

## Praxis-Übung: Der Regisseur und der Schauspieler

Die KI hat keine Persönlichkeit. Sie ist ein Schauspieler, der durch unsere Anweisungen (**Prompts**) in eine Rolle schlüpft. Wir steuern die "Autovervollständigung" durch den Kontext.

**Szenario:** Erinnerung an das Team zur Urlaubsplanung.

### Versuch 1: Ohne Kontext (Der Durchschnitt)
* **Prompt:** "Schreibe eine Mail an das Team wegen Urlaubsplanung."
* **Ergebnis:** Standard-Bürodeutsch. Höflich, aber langweilig.

### Versuch 2: Strenges Amtsdeutsch
* **Prompt:** "Schreibe sehr formell, distanziert, nutze Passiv und Wörter wie 'fristgerecht' und 'obliegt'."
* **Ergebnis:** Die Wahrscheinlichkeit für Wörter wie "hiermit" und "Anordnung" steigt. Der Text wirkt bürokratisch und streng.

### Versuch 3: Locker & Modern
* **Prompt:** "Schreibe extrem locker, per Du, motivierend, nutze Emojis und Jugendsprache."
* **Ergebnis:** Die Wahrscheinlichkeit für "Hey Leute" und "🚀" steigt. Der Text wirkt wie ein Social-Media-Post.

---

## Die 4-Bausteine-Methode für perfekte Prompts

Um im Arbeitsalltag sofort gute Ergebnisse zu erzielen und langes Herumprobieren zu vermeiden, nutzen wir diese Formel:

### Die Formel:
**1. ROLLE** + **2. AUFGABE** + **3. KONTEXT** + **4. FORMAT**

| Baustein | Frage | Beispiel |
| :--- | :--- | :--- |
| **1. Rolle** | Wer soll die KI sein? | "Du bist ein erfahrener Kundendienst-Mitarbeiter..." |
| **2. Aufgabe** | Was soll sie tun? | "...verfasse ein Antwortschreiben..." |
| **3. Kontext** | Worum geht es genau? | "...auf die Beschwerde von Herrn Müller über die falsche Rechnung." |
| **4. Format** | Wie soll es aussehen? | "...fasse dich kurz, sei sehr höflich und nutze eine Liste." |

### Vorher/Nachher Beispiel: Meeting-Zusammenfassung

* ❌ **Schlecht:** "Fass das Meeting zusammen."
    * *Ergebnis:* Unstrukturiert, KI rät, was wichtig war.
* ✅ **Gut:** "Du bist Projektassistent **(Rolle)**. Fasse meine Notizen zusammen **(Aufgabe)**. Es ging um die Software-Einführung und Zeitprobleme **(Kontext)**. Erstelle eine Tabelle mit Spalten 'Thema' und 'Entscheidung' **(Format)**."
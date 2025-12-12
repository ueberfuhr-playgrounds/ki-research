### Das Praxis-Beispiel: Der "Reisekosten-Helfer"

Wir bauen einen Assistenten, damit Office-Nutzer nicht mehr in der 50-seitigen PDF "Reiserichtlinie 2024" blättern müssen, sondern einfach fragen können: *"Darf ich das Taxi von Berlin Hbf zum Hotel abrechnen?"*

#### Schritt 1: Das "Gem" (oder Projekt) erstellen
Wir erstellen die **Persona**.
* **Name:** "Reisekosten-Helfer"
* **Anweisung (System Prompt):** "Du bist ein strenger aber freundlicher Assistent der Buchhaltung. Antworte NUR basierend auf den bereitgestellten Richtlinien. Wenn etwas nicht klar ist, lehne ab."
* *Analogie:* Wir schreiben gerade die Stellenbeschreibung.

#### Schritt 2: RAG vorbereiten (Wissen hochladen)
Wir füttern den Agenten mit Fakten.
* **Aktion:** Wir laden die PDF `Reiserichtlinie_2024_Final.pdf` in das Gem/Projekt hoch.
* *Analogie:* Wir legen dem neuen Mitarbeiter den Ordner auf den Tisch und sagen: "Lerne das auswendig."
* *Technik:* Ab jetzt nutzt der Agent **RAG**. Wenn wir fragen, sucht er erst in der PDF (*Retrieval*) und antwortet dann (*Generation*).

#### Schritt 3: Extensions / Connectors aktivieren (Optional)
Wir geben dem Agenten Zugriff auf E-Mails.
* **Aktion:** Wir aktivieren die "Google Workspace Extension" (bei Gemini) oder verknüpfen Outlook (bei Copilot/Claude via Connectors).
* **User-Frage:** "Habe ich die Hotel-Rechnung aus München schon per Mail bekommen?"
* **Ablauf:** Der **Agent** nutzt das **Modell** um die Frage zu verstehen -> nutzt die **Extension** um im Postfach zu suchen -> findet die Mail -> gleicht sie per **RAG** mit der PDF-Richtlinie ab -> gibt Antwort.

#### Zusammenfassung des Szenarios für die Teilnehmer:

> "Stellen Sie sich vor: Das **Modell** ist das Gehirn, das Deutsch versteht. Das **Gem** ist der Hut 'Buchhalter', den wir ihm aufsetzen. Die **PDF** ist das Regelbuch, in dem er per **RAG** nachschlägt. Und die **Extension** sind seine Hände, mit denen er in Ihrem Posteingang nach der Rechnung wühlt."
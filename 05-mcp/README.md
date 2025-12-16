# Model Context Protocol (MCP)

> [!NOTE]
> Ziel ist die Darstellung der Funktionsweise von MCP sowie die Architektur von MCP-Client und MCP-Server.

## KI-Prompt

> Lass uns den Lernenden die Architektur und die Kommunikation mit MCP näher bringen. Ziel soll sein, die Unterschiede bei den verschiedenen Ansätzen zu skizzieren:
>
> - Lokaler Subprozess mit STDIO /JSON-RPC
> - Remote-Anwendung mit HTTP (Streaming) bzw. HTTP (SSE)
>
> Wichtig ist zu erkennen, wo die MCP-Anwendung jeweils läuft, und die 3 Phasen (Handshake, Tool-Listen-Abfrage, Aufruf eines Tools) an einem konkreten HalloWelt-Beispiel abzufragen. Im Beispiel soll ein HalloWelt-Backend mit REST-API angesprochen werden können. Die MCP-Serveranwendung dient dann sozusagen als Bridge.
>
> Interessant wäre auch, die möglichen OAuth-Flows zu vergleichen.
>
> Erstelle zunächst eine Beschreibung der unterschiedlichen Szenarien mit Markdown-Quellcode. Gerne vergleiche auch in tabellarischer Form.

## Ergebnisse

- [Text-Version](erklaerung.md)

## Visualisierungs-Prompt

> Ja, erstelle eine Visualisierung für die beiden Szenarien lokal und remote. Die Authentifizierung muss da nicht unbedingt mit rein. Aber die 3 Phasen (Handshake, Tool-Liste, Aufruf eines HalloWelt-Tools, das dann umwandelt in einen REST-API-Call zum eigentlichen Backend), gerne mit konkretem JSON-RPC in der Darstellung. Vor allem wichtig wäre die Verteilung der 3 Systeme (KI-Agent, MCP-Server, REST-Backend) zu sehen.

> [!NOTE]
> Es folgten noch ein paar Korrekturschleifen, die hier nicht dokumentiert sind.

## Ergebnisse

- [Visualisierung](visualisierung.html)

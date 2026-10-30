# CEO-AI-Briefing-Agent

Entwicklung eines automatisierten Market-Intelligence-Workflows (n8n & Gemini-API) zur Echtzeit-Aggregation von Finanznachrichten und Erstellung strukturierter Top-Down-Management-Briefings. Dieses Proof of Concept (PoC) wurde entwickelt, um strategische Informationsflüsse für das C-Level zu optimieren.

## ⚙️ Architektur & Prozessablauf

![n8n Workflow Architektur]("C:\Users\momow\Downloads\n8n_CEO-Briefing.png")
*(Hinweis: Dateipfad des hochgeladenen Workflow-Bildes hier einfügen)*

Der Workflow läuft vollautomatisiert täglich um 06:00 Uhr ab und durchläuft drei Kernphasen:

1. **Datenbeschaffung & Vorfilterung:** Paralleler Abruf relevanter Finanz-RSS-Feeds (Handelsblatt, Financial Times, Reuters etc.). Ein integriertes Keyword-Routing filtert irrelevantes Rauschen heraus und isoliert strategisch bedeutsame Artikel zu Makroökonomie, direkten Wettbewerbern und Regulatorik.
2. **KI-Analyse & Strukturierung (Gemini API):** Die gebündelten Rohdaten werden als formatiertes JSON an das LLM übergeben. Das Modell übersetzt englische Kerninformationen und kategorisiert die Daten in feste strategische Säulen.
3. **Automatisierte Auslieferung:** Das final generierte Briefing wird über einen dedizierten Microsoft Outlook-Node als strukturierte E-Mail an das CEO-Office versendet.

## 📊 Ergebnis: Das Executive Briefing

![Finales E-Mail Briefing]("C:\Users\momow\Downloads\Mail_CEO-Briefing.png")
*(Hinweis: Dateipfad des hochgeladenen E-Mail-Bildes hier einfügen)*

Das Output-Format liefert dem Management eine sofortige Übersicht der aktuellen Marktdynamik. Das LLM ist dabei so konfiguriert, dass es fehlende Marktbewegungen in spezifischen Sektoren proaktiv als "Keine signifikanten Meldungen" deklariert, um eine effiziente Informationsaufnahme zu garantieren.

## 🛠 Tech Stack
* **Automation Engine:** n8n (Node-based Workflow Automation)
* **KI / LLM:** Google Gemini 3.8 Flash API
* **Datenquellen:** RSS-Feeds (XML/JSON Parsing)
* **Integrationen:** Microsoft Outlook API

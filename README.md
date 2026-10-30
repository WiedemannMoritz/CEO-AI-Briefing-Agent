# CEO-AI-Briefing-Agent

Entwicklung eines automatisierten Market-Intelligence-Workflows (n8n & Gemini-API) zur Echtzeit-Aggregation von Finanznachrichten und Erstellung strukturierter Top-Down-Management-Briefings. Dieses Proof of Concept (PoC) wurde entwickelt, um strategische Informationsflüsse für das C-Level zu optimieren.

## ⚙️ Architektur & Prozessablauf

<img width="918" height="343" alt="n8n_CEO-Briefing" src="https://github.com/user-attachments/assets/6de1d08e-2bc8-4335-b7fc-5752bda1508b" />

Der Workflow läuft vollautomatisiert täglich um 06:00 Uhr ab und durchläuft drei Kernphasen:

1. **Datenbeschaffung & Vorfilterung:** Paralleler Abruf relevanter Finanz-RSS-Feeds (Handelsblatt, Financial Times, Reuters etc.). Ein integriertes Keyword-Routing filtert irrelevantes Rauschen heraus und isoliert strategisch bedeutsame Artikel zu Makroökonomie, direkten Wettbewerbern und Regulatorik.
2. **KI-Analyse & Strukturierung (Gemini API):** Die gebündelten Rohdaten werden als formatiertes JSON an das LLM übergeben. Das Modell übersetzt englische Kerninformationen und kategorisiert die Daten in feste strategische Säulen.
3. **Automatisierte Auslieferung:** Das final generierte Briefing wird über einen dedizierten Microsoft Outlook-Node als strukturierte E-Mail an das CEO-Office versendet.

## 📊 Ergebnis: Das Executive Briefing

<img width="1040" height="288" alt="Mail_CEO-Briefing" src="https://github.com/user-attachments/assets/d042c59f-3c2e-44e2-8898-cca77ba7ea7d" />

Das Output-Format liefert dem Management eine sofortige Übersicht der aktuellen Marktdynamik. Das LLM ist dabei so konfiguriert, dass es fehlende Marktbewegungen in spezifischen Sektoren proaktiv als "Keine signifikanten Meldungen" deklariert, um eine effiziente Informationsaufnahme zu garantieren.

## 🛠 Tech Stack
* **Automation Engine:** n8n (Node-based Workflow Automation)
* **KI / LLM:** Google Gemini 3.8 Flash API
* **Datenquellen:** RSS-Feeds (XML/JSON Parsing)
* **Integrationen:** Microsoft Outlook API

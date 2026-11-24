# Projekte


{# Keep relevance scores aligned with the other language. Higher scores appear first. #}
{% set projects = [
    { "name": "Ryllis", "relevance": 70, "slug": "ryllis",
      "summary": "Ein Static-Site-Generator für mehrsprachige Websites aus Markdown und MiniJinja-Vorlagen. Er erzeugt auch diese Website." },
    { "name": "Sanqi", "relevance": 60, "slug": "sanqi",
      "summary": "Eine in Rust entwickelte Spiel-Engine für das Brettspiel Sanqi (三棋) mit einer mehrsprachigen mobilen App." },
    { "name": "Rimbun", "relevance": 50, "slug": "rimbun",
      "summary": "Eine experimentelle Plattform zum gemeinsamen Schreiben, Vergleichen und Bearbeiten alternativer Fassungen einzelner Dokumentabschnitte." },
    { "name": "Spreat", "relevance": 40, "slug": "spreat",
      "summary": "Ein Browserspiel-Prototyp, bei dem Spieler Atome auf einem Sechseckraster platzieren und Kettenreaktionen auslösen." },
    { "name": "Mehrkat", "relevance": 30, "slug": "mehrkat",
      "summary": "Ein KI-gestütztes Werkzeug, das Börsennachrichten zusammenfasst und die Quellen angibt." },
    { "name": "Slofox", "relevance": 20, "slug": "slofox",
      "summary": "Ein Prototyp mit Rust und Bevy, in dem zwei animierte Talkshow-Moderatoren in einem 3D-Studio auf Live-Audio reagieren." },
    { "name": "TrayStack", "relevance": 10, "slug": "traystack",
      "summary": "Ein lokaler Prototyp zur Vertragsablage und Volltextsuche, der Fundstellen in den Originaldokumenten nachvollziehbar macht." },
] %}

{% for project in projects | sort(attribute="relevance", reverse=true) %}
## [{{ project.name }}]({{ project.slug }}.html)

{{ project.summary }}

{% endfor %}

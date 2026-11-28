# Projekte


{# Keep relevance scores aligned with the other language. Higher scores appear first. #}
{% set projects = [
    { "name": "Ryllis", "relevance": 70, "slug": "ryllis",
      "summary": "Ryllis erzeugt mehrsprachige statische Websites aus Markdown und MiniJinja. Es ordnet Übersetzungen anhand ihrer Dateipfade zu, prüft Links und meldet fehlende Übersetzungen vor der Veröffentlichung." },
    { "name": "Sanqi", "relevance": 60, "slug": "sanqi",
      "summary": "Sanqi ist eine in Rust entwickelte Engine für das Brettspiel Sanqi (三棋). Im mehrsprachigen Mobilprototyp und auf der Kommandozeile können Menschen oder der Computer die beiden Seiten übernehmen." },
    { "name": "Rimbun", "relevance": 50, "slug": "rimbun",
      "summary": "Rimbun ist eine experimentelle Plattform zum gemeinsamen Schreiben. Leser können eine Hauptfassung ansehen und veröffentlichte Alternativen Abschnitt für Abschnitt vergleichen." },
    { "name": "Spreat", "relevance": 40, "slug": "spreat",
      "summary": "Spreat ist ein Browserspiel-Prototyp auf einem sechseckigen Raster. Spieler setzen Atome, die sich beim Explodieren auf Nachbarfelder verteilen und Kettenreaktionen auslösen können." },
    { "name": "Mehrkat", "relevance": 30, "slug": "mehrkat",
      "summary": "Mehrkat erstellt KI-gestützte Zusammenfassungen von Börsennachrichten. Nach der Auswahl eines Unternehmens oder Tickers und einer Börsennotierung führen Quellenangaben zu den zugrunde liegenden Beiträgen." },
    { "name": "Slofox", "relevance": 20, "slug": "slofox",
      "summary": "Slofox zeigt zwei animierte Talkshow-Moderatoren in einem 3D-Studio. Eine Figur reagiert auf den Ton aus dem Browser, die andere auf ein Mikrofon. So lässt sich ein Gespräch inszenieren und aufzeichnen." },
    { "name": "TrayStack", "relevance": 10, "slug": "traystack",
      "summary": "TrayStack ist ein lokaler Prototyp für die Ablage und Suche in Verträgen. Suchergebnisse führen zu den jeweiligen Fundstellen zurück, damit sie sich im Zusammenhang prüfen lassen." },
] %}

{% for project in projects | sort(attribute="relevance", reverse=true) %}
## [{{ project.name }}![]({% if project.slug == "sanqi" %}/assets/sanqi/app-icon.svg{% elif project.slug == "ryllis" %}/assets/projects/ryllis.png{% else %}/assets/projects/{{ project.slug }}.svg{% endif %})]({{ project.slug }}.html)

{{ project.summary }}

{% endfor %}

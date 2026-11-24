# Projects


{# Keep relevance scores aligned with the other language. Higher scores appear first. #}
{% set projects = [
    { "name": "Ryllis", "relevance": 70, "slug": "ryllis",
      "summary": "A static site generator for multilingual Markdown sites with MiniJinja templates. It builds this website." },
    { "name": "Sanqi", "relevance": 60, "slug": "sanqi",
      "summary": "A Rust engine for the Sanqi (三棋) board game, with a multilingual mobile app." },
    { "name": "Rimbun", "relevance": 50, "slug": "rimbun",
      "summary": "An experimental collaborative writing platform for comparing and editing alternative versions of document sections." },
    { "name": "Spreat", "relevance": 40, "slug": "spreat",
      "summary": "A browser game prototype where players place atoms on a hexagonal grid and trigger chain reactions." },
    { "name": "Mehrkat", "relevance": 30, "slug": "mehrkat",
      "summary": "An AI-assisted tool that summarizes stock news and cites its sources." },
    { "name": "Slofox", "relevance": 20, "slug": "slofox",
      "summary": "A Rust and Bevy prototype with two animated talk-show hosts that respond to live audio in a 3D studio." },
    { "name": "TrayStack", "relevance": 10, "slug": "traystack",
      "summary": "A local prototype for storing contracts and tracing full-text search results back to passages in the original documents." },
] %}

{% for project in projects | sort(attribute="relevance", reverse=true) %}
## [{{ project.name }}]({{ project.slug }}.html)

{{ project.summary }}

{% endfor %}

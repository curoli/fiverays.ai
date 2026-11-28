# Projects


{# Keep relevance scores aligned with the other language. Higher scores appear first. #}
{% set projects = [
    { "name": "Ryllis", "relevance": 70, "slug": "ryllis",
      "summary": "Ryllis builds multilingual static sites from Markdown and MiniJinja. It pairs translations by file path and can check links and report missing translations before you publish." },
    { "name": "Sanqi", "relevance": 60, "slug": "sanqi",
      "summary": "Sanqi is a Rust engine for the board game Sanqi (三棋). You can play in a multilingual mobile prototype or from the command line, with human or computer players." },
    { "name": "Rimbun", "relevance": 50, "slug": "rimbun",
      "summary": "Rimbun is an experimental platform for writing together. Readers can see a main version of a document and compare published alternatives section by section." },
    { "name": "Spreat", "relevance": 40, "slug": "spreat",
      "summary": "Spreat is a browser game prototype played on a hexagonal board. Players place atoms that can burst, spread to neighboring cells, and set off chain reactions." },
    { "name": "Mehrkat", "relevance": 30, "slug": "mehrkat",
      "summary": "Mehrkat creates AI-assisted briefings on stock news. Choose a company or ticker and a listing, then follow the citations to the sources behind the summary." },
    { "name": "Slofox", "relevance": 20, "slug": "slofox",
      "summary": "Slofox renders two animated talk-show hosts in a 3D studio. One responds to browser audio and the other to a microphone, so a conversation can be staged and recorded." },
    { "name": "TrayStack", "relevance": 10, "slug": "traystack",
      "summary": "TrayStack is a local prototype for storing and searching contracts. Search results point back to the passages they came from, so findings can be reviewed in context." },
] %}

{% for project in projects | sort(attribute="relevance", reverse=true) %}
## [{{ project.name }}{% if project.slug == "sanqi" %}![](/assets/sanqi/app-icon.svg){% endif %}]({{ project.slug }}.html)

{{ project.summary }}

{% endfor %}

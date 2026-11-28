# Projets

{% set projects = [
  {
    "name": "Ryllis",
    "relevance": 70,
    "slug": "ryllis",
    "summary": "Générateur de sites statiques multilingues à partir de Markdown et MiniJinja, avec vérification des liens et des traductions."
  },
  {
    "name": "Sanqi",
    "relevance": 60,
    "slug": "sanqi",
    "summary": "Moteur Rust du jeu Sanqi (三棋), jouable sur mobile ou en ligne de commande, contre une personne ou l’ordinateur."
  },
  {
    "name": "Rimbun",
    "relevance": 50,
    "slug": "rimbun",
    "summary": "Plateforme expérimentale d’écriture collaborative et de comparaison des variantes publiées section par section."
  },
  {
    "name": "Spreat",
    "relevance": 40,
    "slug": "spreat",
    "summary": "Jeu sur navigateur où des atomes éclatent sur un plateau hexagonal et déclenchent des réactions en chaîne."
  },
  {
    "name": "Mehrkat",
    "relevance": 30,
    "slug": "mehrkat",
    "summary": "Synthèses de l’actualité boursière assistées par IA, avec des liens vers les sources."
  },
  {
    "name": "Slofox",
    "relevance": 20,
    "slug": "slofox",
    "summary": "Deux animateurs en 3D réagissent à l’audio du navigateur et du microphone dans un studio virtuel."
  },
  {
    "name": "TrayStack",
    "relevance": 10,
    "slug": "traystack",
    "summary": "Prototype local qui recherche des passages dans les contrats et les restitue dans leur contexte."
  }
] %}

{% for project in projects | sort(attribute="relevance", reverse=true) %}
## [{{ project.name }}![]({% if project.slug == "sanqi" %}/assets/sanqi/app-icon.svg{% elif project.slug == "ryllis" %}/assets/projects/ryllis.png{% else %}/assets/projects/{{ project.slug }}.svg{% endif %})]({{ project.slug }}.html)

{{ project.summary }}

{% endfor %}

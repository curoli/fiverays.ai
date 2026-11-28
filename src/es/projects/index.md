# Proyectos

{% set projects = [
  {
    "name": "Ryllis",
    "relevance": 70,
    "slug": "ryllis",
    "summary": "Generador de sitios estáticos multilingües con Markdown y MiniJinja que comprueba enlaces y traducciones."
  },
  {
    "name": "Sanqi",
    "relevance": 60,
    "slug": "sanqi",
    "summary": "Motor Rust para el juego Sanqi (三棋), con prototipo móvil y línea de comandos para jugar contra otra persona o contra el ordenador."
  },
  {
    "name": "Rimbun",
    "relevance": 50,
    "slug": "rimbun",
    "summary": "Plataforma experimental de escritura colaborativa con alternativas publicadas por sección."
  },
  {
    "name": "Spreat",
    "relevance": 40,
    "slug": "spreat",
    "summary": "Juego de navegador en un tablero hexagonal donde los átomos estallan en cadena."
  },
  {
    "name": "Mehrkat",
    "relevance": 30,
    "slug": "mehrkat",
    "summary": "Informes de noticias bursátiles asistidos por IA, con citas para consultar las fuentes."
  },
  {
    "name": "Slofox",
    "relevance": 20,
    "slug": "slofox",
    "summary": "Dos presentadores animados reaccionan al navegador y al micrófono en un estudio 3D."
  },
  {
    "name": "TrayStack",
    "relevance": 10,
    "slug": "traystack",
    "summary": "Prototipo local para encontrar y revisar pasajes de contratos en contexto."
  }
] %}

{% for project in projects | sort(attribute="relevance", reverse=true) %}
## [{{ project.name }}{% if project.slug == "sanqi" %}![](/assets/sanqi/app-icon.svg){% endif %}]({{ project.slug }}.html)

{{ project.summary }}

{% endfor %}

# Projetos

{% set projects = [
  {
    "name": "Ryllis",
    "relevance": 70,
    "slug": "ryllis",
    "summary": "Gerador de sítios estáticos multilingues com Markdown e MiniJinja e verificação de ligações e traduções."
  },
  {
    "name": "Sanqi",
    "relevance": 60,
    "slug": "sanqi",
    "summary": "Motor em Rust para o jogo Sanqi (三棋), jogável no protótipo móvel ou na linha de comandos contra uma pessoa ou o computador."
  },
  {
    "name": "Rimbun",
    "relevance": 50,
    "slug": "rimbun",
    "summary": "Plataforma experimental para escrever em conjunto e comparar versões publicadas por secção."
  },
  {
    "name": "Spreat",
    "relevance": 40,
    "slug": "spreat",
    "summary": "Jogo de navegador em que átomos rebentam e desencadeiam reações em cadeia num tabuleiro hexagonal."
  },
  {
    "name": "Mehrkat",
    "relevance": 30,
    "slug": "mehrkat",
    "summary": "Resumos de notícias da bolsa com assistência de IA e ligações para as fontes."
  },
  {
    "name": "Slofox",
    "relevance": 20,
    "slug": "slofox",
    "summary": "Dois apresentadores animados num estúdio 3D reagem ao som do navegador e do microfone."
  },
  {
    "name": "TrayStack",
    "relevance": 10,
    "slug": "traystack",
    "summary": "Protótipo local para pesquisar e rever excertos de contratos em contexto."
  }
] %}

{% for project in projects | sort(attribute="relevance", reverse=true) %}
## [{{ project.name }}{% if project.slug == "sanqi" %}![](/assets/sanqi/app-icon.svg){% endif %}]({{ project.slug }}.html)

{{ project.summary }}

{% endfor %}

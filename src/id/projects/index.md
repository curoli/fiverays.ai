# Proyek

{% set projects = [
  {
    "name": "Ryllis",
    "relevance": 70,
    "slug": "ryllis",
    "summary": "Generator situs statis multibahasa berbasis Markdown dan MiniJinja dengan pemeriksaan tautan dan terjemahan."
  },
  {
    "name": "Sanqi",
    "relevance": 60,
    "slug": "sanqi",
    "summary": "Mesin Rust untuk gim papan Sanqi (三棋) di perangkat seluler atau baris perintah."
  },
  {
    "name": "Rimbun",
    "relevance": 50,
    "slug": "rimbun",
    "summary": "Platform eksperimental untuk menulis bersama dan membandingkan versi setiap bagian."
  },
  {
    "name": "Spreat",
    "relevance": 40,
    "slug": "spreat",
    "summary": "Gim peramban dengan ledakan atom berantai di papan heksagonal."
  },
  {
    "name": "Mehrkat",
    "relevance": 30,
    "slug": "mehrkat",
    "summary": "Ringkasan berita saham berbantuan AI dengan rujukan sumber."
  },
  {
    "name": "Slofox",
    "relevance": 20,
    "slug": "slofox",
    "summary": "Dua pembawa acara animasi menanggapi audio peramban dan mikrofon di studio 3D."
  },
  {
    "name": "TrayStack",
    "relevance": 10,
    "slug": "traystack",
    "summary": "Prototipe lokal untuk mencari dan meninjau kutipan kontrak."
  }
] %}

{% for project in projects | sort(attribute="relevance", reverse=true) %}
## [{{ project.name }}]({{ project.slug }}.html)

{{ project.summary }}

{% endfor %}

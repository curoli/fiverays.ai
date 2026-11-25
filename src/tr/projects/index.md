# Projeler

{% set projects = [
  {
    "name": "Ryllis",
    "relevance": 70,
    "slug": "ryllis",
    "summary": "Markdown ve MiniJinja ile çok dilli statik siteler oluşturur ve bağlantılarla çevirileri denetler."
  },
  {
    "name": "Sanqi",
    "relevance": 60,
    "slug": "sanqi",
    "summary": "Mobil prototipten veya komut satırından oynanan Sanqi (三棋) için Rust motoru."
  },
  {
    "name": "Rimbun",
    "relevance": 50,
    "slug": "rimbun",
    "summary": "Birlikte yazma ve yayımlanan bölüm sürümlerini karşılaştırma platformu."
  },
  {
    "name": "Spreat",
    "relevance": 40,
    "slug": "spreat",
    "summary": "Altıgen tahtada atom patlamalarıyla zincirleme tepkimeler oluşturan tarayıcı oyunu."
  },
  {
    "name": "Mehrkat",
    "relevance": 30,
    "slug": "mehrkat",
    "summary": "Kaynaklı borsa haberleri için yapay zekâ destekli özetler."
  },
  {
    "name": "Slofox",
    "relevance": 20,
    "slug": "slofox",
    "summary": "3B stüdyoda tarayıcı ve mikrofon sesine tepki veren iki animasyonlu sunucu."
  },
  {
    "name": "TrayStack",
    "relevance": 10,
    "slug": "traystack",
    "summary": "Sözleşme bölümlerini bağlamıyla bulmaya ve incelemeye yarayan yerel prototip."
  }
] %}

{% for project in projects | sort(attribute="relevance", reverse=true) %}
## [{{ project.name }}]({{ project.slug }}.html)

{{ project.summary }}

{% endfor %}

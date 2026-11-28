# প্রকল্প

{% set projects = [
  {
    "name": "Ryllis",
    "relevance": 70,
    "slug": "ryllis",
    "summary": "Markdown ও MiniJinja দিয়ে বহুভাষিক স্থির সাইট তৈরি এবং লিংক ও অনুবাদ পরীক্ষা।"
  },
  {
    "name": "Sanqi",
    "relevance": 60,
    "slug": "sanqi",
    "summary": "মোবাইল বা কমান্ড লাইনে খেলার জন্য Sanqi (三棋) বোর্ড গেমের Rust ইঞ্জিন।"
  },
  {
    "name": "Rimbun",
    "relevance": 50,
    "slug": "rimbun",
    "summary": "যৌথ লেখালেখি ও প্রতি অংশে প্রকাশিত সংস্করণ তুলনার পরীক্ষামূলক প্ল্যাটফর্ম।"
  },
  {
    "name": "Spreat",
    "relevance": 40,
    "slug": "spreat",
    "summary": "ষড়ভুজ বোর্ডে পরমাণুর বিস্ফোরণ ও শৃঙ্খল বিক্রিয়ার ব্রাউজার গেম।"
  },
  {
    "name": "Mehrkat",
    "relevance": 30,
    "slug": "mehrkat",
    "summary": "উৎসসহ শেয়ারবাজারের খবরের AI-সহায়িত সারাংশ।"
  },
  {
    "name": "Slofox",
    "relevance": 20,
    "slug": "slofox",
    "summary": "3D স্টুডিওতে ব্রাউজার ও মাইক্রোফোনের শব্দে সাড়া দেন দুই উপস্থাপক।"
  },
  {
    "name": "TrayStack",
    "relevance": 10,
    "slug": "traystack",
    "summary": "চুক্তির অংশ খুঁজে প্রাসঙ্গিকভাবে পর্যালোচনার স্থানীয় প্রোটোটাইপ।"
  }
] %}

{% for project in projects | sort(attribute="relevance", reverse=true) %}
## [{{ project.name }}![]({% if project.slug == "sanqi" %}/assets/sanqi/app-icon.svg{% elif project.slug == "ryllis" %}/assets/projects/ryllis.png{% else %}/assets/projects/{{ project.slug }}.svg{% endif %})]({{ project.slug }}.html)

{{ project.summary }}

{% endfor %}

# المشاريع

{% set projects = [
  {
    "name": "Ryllis",
    "relevance": 70,
    "slug": "ryllis",
    "summary": "مولّد مواقع ثابتة متعددة اللغات من Markdown وMiniJinja مع فحص الروابط والترجمات."
  },
  {
    "name": "Sanqi",
    "relevance": 60,
    "slug": "sanqi",
    "summary": "محرّك Rust للعبة Sanqi ‏(三棋)، للهواتف وسطر الأوامر."
  },
  {
    "name": "Rimbun",
    "relevance": 50,
    "slug": "rimbun",
    "summary": "منصّة تجريبية للكتابة المشتركة ومقارنة النسخ المنشورة لكل قسم."
  },
  {
    "name": "Spreat",
    "relevance": 40,
    "slug": "spreat",
    "summary": "لعبة متصفح تنفجر فيها الذرات على لوحة سداسية لتطلق تفاعلات متسلسلة."
  },
  {
    "name": "Mehrkat",
    "relevance": 30,
    "slug": "mehrkat",
    "summary": "موجزات لأخبار الأسهم بمساعدة الذكاء الاصطناعي مع إحالات إلى المصادر."
  },
  {
    "name": "Slofox",
    "relevance": 20,
    "slug": "slofox",
    "summary": "مقدّمان متحركان يستجيبان لصوت المتصفح والميكروفون في استوديو ثلاثي الأبعاد."
  },
  {
    "name": "TrayStack",
    "relevance": 10,
    "slug": "traystack",
    "summary": "نموذج محلي للبحث عن مقاطع العقود ومراجعتها في سياقها."
  }
] %}

{% for project in projects | sort(attribute="relevance", reverse=true) %}
## [{{ project.name }}{% if project.slug == "sanqi" %}![](/assets/sanqi/app-icon.svg){% endif %}]({{ project.slug }}.html)

{{ project.summary }}

{% endfor %}

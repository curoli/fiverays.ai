# منصوبے

{% set projects = [
  {
    "name": "Ryllis",
    "relevance": 70,
    "slug": "ryllis",
    "summary": "Markdown اور MiniJinja سے کثیر لسانی اسٹیٹک سائٹس اور لنکس اور تراجم کی جانچ۔"
  },
  {
    "name": "Sanqi",
    "relevance": 60,
    "slug": "sanqi",
    "summary": "Sanqi (三棋) بورڈ گیم کا Rust انجن، موبائل یا کمانڈ لائن پر کھیلنے کے لیے۔"
  },
  {
    "name": "Rimbun",
    "relevance": 50,
    "slug": "rimbun",
    "summary": "مل کر لکھنے اور شائع شدہ متبادل حصوں کا موازنہ کرنے کا تجرباتی پلیٹ فارم۔"
  },
  {
    "name": "Spreat",
    "relevance": 40,
    "slug": "spreat",
    "summary": "مسدسی بورڈ پر ایٹموں کے سلسلہ وار دھماکوں والی براؤزر گیم۔"
  },
  {
    "name": "Mehrkat",
    "relevance": 30,
    "slug": "mehrkat",
    "summary": "مصنوعی ذہانت کی مدد سے حصص کی خبروں کے خلاصے، اصل حوالوں کے ساتھ۔"
  },
  {
    "name": "Slofox",
    "relevance": 20,
    "slug": "slofox",
    "summary": "تھری ڈی اسٹوڈیو میں دو میزبان براؤزر اور مائیکروفون کی آڈیو پر ردعمل دیتے ہیں۔"
  },
  {
    "name": "TrayStack",
    "relevance": 10,
    "slug": "traystack",
    "summary": "معاہدوں کے اقتباسات تلاش اور سیاق میں جانچنے کا مقامی پروٹوٹائپ۔"
  }
] %}

{% for project in projects | sort(attribute="relevance", reverse=true) %}
## [{{ project.name }}]({{ project.slug }}.html)

{{ project.summary }}

{% endfor %}

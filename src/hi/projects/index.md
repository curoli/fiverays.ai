# परियोजनाएँ

{% set projects = [
  {
    "name": "Ryllis",
    "relevance": 70,
    "slug": "ryllis",
    "summary": "Markdown और MiniJinja से बहुभाषी साइट बनाता है और लिंक व अनुवाद जाँचता है।"
  },
  {
    "name": "Sanqi",
    "relevance": 60,
    "slug": "sanqi",
    "summary": "Sanqi (三棋) बोर्ड गेम का Rust इंजन, मोबाइल या कमांड लाइन पर खेलने के लिए।"
  },
  {
    "name": "Rimbun",
    "relevance": 50,
    "slug": "rimbun",
    "summary": "सहयोगी लेखन और प्रकाशित खंडों की तुलना के लिए प्रयोगात्मक मंच।"
  },
  {
    "name": "Spreat",
    "relevance": 40,
    "slug": "spreat",
    "summary": "षट्भुज बोर्ड पर परमाणुओं के विस्फोट की श्रृंखला वाला ब्राउज़र गेम।"
  },
  {
    "name": "Mehrkat",
    "relevance": 30,
    "slug": "mehrkat",
    "summary": "स्रोतों के साथ शेयर समाचारों का AI-सहायित सार।"
  },
  {
    "name": "Slofox",
    "relevance": 20,
    "slug": "slofox",
    "summary": "3D स्टूडियो में ब्राउज़र और माइक्रोफ़ोन की ध्वनि पर प्रतिक्रिया देने वाले दो प्रस्तुतकर्ता।"
  },
  {
    "name": "TrayStack",
    "relevance": 10,
    "slug": "traystack",
    "summary": "अनुबंधों में अंश खोजने और संदर्भ सहित जाँचने का स्थानीय प्रोटोटाइप।"
  }
] %}

{% for project in projects | sort(attribute="relevance", reverse=true) %}
## [{{ project.name }}{% if project.slug == "sanqi" %}![](/assets/sanqi/app-icon.svg){% endif %}]({{ project.slug }}.html)

{{ project.summary }}

{% endfor %}

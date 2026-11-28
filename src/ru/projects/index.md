# Проекты

{% set projects = [
  {
    "name": "Ryllis",
    "relevance": 70,
    "slug": "ryllis",
    "summary": "Генератор многоязычных статических сайтов из Markdown и MiniJinja с проверкой ссылок и переводов."
  },
  {
    "name": "Sanqi",
    "relevance": 60,
    "slug": "sanqi",
    "summary": "Движок на Rust для игры Sanqi (三棋) на телефоне или в командной строке."
  },
  {
    "name": "Rimbun",
    "relevance": 50,
    "slug": "rimbun",
    "summary": "Экспериментальная платформа для совместной работы над текстом и сравнения версий разделов."
  },
  {
    "name": "Spreat",
    "relevance": 40,
    "slug": "spreat",
    "summary": "Браузерная игра, где атомы взрываются на шестиугольном поле и вызывают цепные реакции."
  },
  {
    "name": "Mehrkat",
    "relevance": 30,
    "slug": "mehrkat",
    "summary": "Обзоры биржевых новостей с помощью ИИ и ссылками на источники."
  },
  {
    "name": "Slofox",
    "relevance": 20,
    "slug": "slofox",
    "summary": "Два анимированных ведущих реагируют на звук браузера и микрофона в 3D-студии."
  },
  {
    "name": "TrayStack",
    "relevance": 10,
    "slug": "traystack",
    "summary": "Локальный прототип для поиска и проверки фрагментов договоров в контексте."
  }
] %}

{% for project in projects | sort(attribute="relevance", reverse=true) %}
## [{{ project.name }}{% if project.slug == "sanqi" %}![](/assets/sanqi/app-icon.svg){% endif %}]({{ project.slug }}.html)

{{ project.summary }}

{% endfor %}

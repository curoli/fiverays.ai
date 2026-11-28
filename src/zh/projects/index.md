# 项目

{% set projects = [
  {
    "name": "Ryllis",
    "relevance": 70,
    "slug": "ryllis",
    "summary": "从 Markdown 和 MiniJinja 生成多语言静态站点，可检查链接和缺失译文。"
  },
  {
    "name": "Sanqi",
    "relevance": 60,
    "slug": "sanqi",
    "summary": "用 Rust 实现的三棋引擎，可在移动端或命令行中与真人或电脑对弈。"
  },
  {
    "name": "Rimbun",
    "relevance": 50,
    "slug": "rimbun",
    "summary": "用于协作写作和逐节对比已发布版本的实验平台。"
  },
  {
    "name": "Spreat",
    "relevance": 40,
    "slug": "spreat",
    "summary": "在六边形棋盘上以原子爆炸触发连锁反应的网页游戏。"
  },
  {
    "name": "Mehrkat",
    "relevance": 30,
    "slug": "mehrkat",
    "summary": "使用 AI 生成带来源引用的股票新闻简报。"
  },
  {
    "name": "Slofox",
    "relevance": 20,
    "slug": "slofox",
    "summary": "两位动画主持人在 3D 演播室中分别响应浏览器和麦克风音频。"
  },
  {
    "name": "TrayStack",
    "relevance": 10,
    "slug": "traystack",
    "summary": "在本地搜索合同并在上下文中审阅相关段落的原型。"
  }
] %}

{% for project in projects | sort(attribute="relevance", reverse=true) %}
## [{{ project.name }}![]({% if project.slug == "sanqi" %}/assets/sanqi/app-icon.svg{% elif project.slug == "ryllis" %}/assets/projects/ryllis.png{% else %}/assets/projects/{{ project.slug }}.svg{% endif %})]({{ project.slug }}.html)

{{ project.summary }}

{% endfor %}

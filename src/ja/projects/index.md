# プロジェクト

{% set projects = [
  {
    "name": "Ryllis",
    "relevance": 70,
    "slug": "ryllis",
    "summary": "Markdown と MiniJinja から多言語サイトを生成し、リンクや未翻訳ページを検査します。"
  },
  {
    "name": "Sanqi",
    "relevance": 60,
    "slug": "sanqi",
    "summary": "ボードゲーム三棋の Rust エンジン。モバイルやコマンドラインで対戦できます。"
  },
  {
    "name": "Rimbun",
    "relevance": 50,
    "slug": "rimbun",
    "summary": "共同執筆と、節ごとの公開済み別案の比較を支援する実験的なサービス。"
  },
  {
    "name": "Spreat",
    "relevance": 40,
    "slug": "spreat",
    "summary": "六角形の盤面で原子が爆発し、連鎖反応を起こすブラウザーゲーム。"
  },
  {
    "name": "Mehrkat",
    "relevance": 30,
    "slug": "mehrkat",
    "summary": "出典を確認できる AI 支援の株式ニュース要約。"
  },
  {
    "name": "Slofox",
    "relevance": 20,
    "slug": "slofox",
    "summary": "3D スタジオで、ブラウザーとマイクの音声に反応する二人の司会者。"
  },
  {
    "name": "TrayStack",
    "relevance": 10,
    "slug": "traystack",
    "summary": "契約書の該当箇所を文脈の中で検索・確認するローカル試作版。"
  }
] %}

{% for project in projects | sort(attribute="relevance", reverse=true) %}
## [{{ project.name }}{% if project.slug == "sanqi" %}![](/assets/sanqi/app-icon.svg){% endif %}]({{ project.slug }}.html)

{{ project.summary }}

{% endfor %}

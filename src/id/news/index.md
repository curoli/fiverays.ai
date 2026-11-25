# Berita

{% set headlines = {"news/2026/11/24-new-website.md": "Situs web baru kami"} %}
{% for article in pages | sort(attribute="path", reverse=true) if article.path[:5] == "news/" and article.path[9:10] == "/" and article.path[12:13] == "/" %}
{% set filename = article.path[13:] %}
{% set date = article.path[5:15] | replace("/", "-") %}
- {{ date }} · [{{ headlines[article.path] | default(filename[3:-3] | replace("-", " ") | capitalize) }}]({{ article.url }})
{%- endfor %}

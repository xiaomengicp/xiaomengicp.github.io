---
layout: page
title: Home
id: home
permalink: /
---

# 你好！

<p style="padding: 3em 1em; background: #f5f7ff; border-radius: 4px;">

  我是乔晓萌，一名[[受训中的精神分析师]]与[[作为创作者的身份认同|创作者]]。欢迎你浏览我的[[数字花园]]，这里是我随时更新、不断生长的思考，它们不完整、粗糙，但或有生机。
  <br><br>
  「过渡空间」是一个精神分析领域的概念，指代某一空间既不属于内在意识或想象的世界，也不属于可观察的外部世界，我想把它用在此处恰好合适。
  <br><br>
  你可以从本页目录开始探索花园，各个笔记之间或有一些相互关联，敬请随意游走，或查看花园的<a class="internal-link" href="/graph">关系图谱</a>；你也可以首先了解[[关于我]]，[[关于站点]]，或者查看站点的[[更新日志]]。
  <br><br>
  祝你玩耍愉快！

<br>

</p>

<strong>写作</strong>
<ul>
    <li>
      <a class="internal-link" href="/psychoanalytic-practice">精神分析实践</a>
    </li>
    <li>      
      <a class="internal-link" href="/psychoanalytic-training">精神分析训练</a>
    </li>
    <li>
      <a class="internal-link" href="/psychoanalytic-ghost-stories">精神分析百鬼图</a>   
    </li>
    <li>
      <a class="internal-link" href="/theory-notes">理论笔记</a>
    </li>
    <li>
      <a class="internal-link" href="/clinical-notes">临床笔记</a>
    </li>
    <li>
      <a class="internal-link" href="/creation">创作</a>
    </li>
    <li>
      <a class="internal-link" href="/workflow">工作流</a>
    </li>
</ul>
<strong>笔记</strong>
<ul>
    <li>
      <a class="internal-link" href="/classes-notes">课程</a>
    </li>
    <li>      
      <a class="internal-link" href="/books">书籍</a>
    </li>
    <li>
      <a class="internal-link" href="/podcasts">播客</a>   
    </li>
    <li>
      <a class="internal-link" href="/papers">文献</a>
    </li>
    <li>
      <a class="internal-link" href="/films">电影</a>
    </li>
</ul>
<strong>常见名词</strong>

<ul>
  {% for note in site.notes  %}
  {% if note.path contains '03 Wiki' %}
  
      <a class="internal-link" href="{{ note.url }}">{{ note.title }}</a>；
  {% endif%}
  {% endfor %}  
 
</ul>

<strong>最近创建 Last Created</strong>

<ul>
  {% assign recent_notes = site.notes | sort: "created" | reverse %}
  {% for note in recent_notes limit: 5 %}
    <li>
      {{ note.created | date: "%Y-%m-%d" }} — <a class="internal-link" href="{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

<strong>最近更新 Last Updated</strong>

<ul>
  

  {% assign recent_notes = site.notes | sort: "updated" | reverse %}
  {% for note in recent_notes limit: 5 %}
  {% assign updated_date = note.updated | date: "%Y-%m-%d" %} 
  {% assign created_date = note.created | date: "%Y-%m-%d" %}

    <li>
      {{ note.updated | date: "%Y-%m-%d" }} — <a class="internal-link" href="{{ note.url }}">{{ note.title }}  </a>
    </li>

  {% endfor %}
</ul>

<style>
  .wrapper {
    max-width: 46em;
  }
</style>

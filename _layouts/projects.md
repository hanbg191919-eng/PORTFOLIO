---
# Mr. Green Jekyll Theme (https://github.com/MrGreensWorkshop/MrGreen-JekyllTheme)
# Copyright (c) 2022 Mr. Green's Workshop https://www.MrGreensWorkshop.com
# Licensed under MIT

layout: default
# projects page
---
{%- include multi_lng/get-lng-by-url.liquid -%}
{%- assign lng = get_lng -%}

{%- assign project_data = page.page_data | default: site.data.content.projects[lng].page_data -%}

{%- assign project_container_style = nil -%}
{%- if project_data.main.img -%}
  {%- capture project_container_style -%} style="background-image:url('{{ project_data.main.img }}');" {%- endcapture -%}
{%- elsif project_data.main.back_color %}
  {%- capture project_container_style -%} style="background-color:{{ project_data.main.back_color }};" {%- endcapture -%}
{%- endif %}

<div class="multipurpose-container project-heading-container" {{project_container_style}}>
{%- assign color_style = nil -%}
{%- if project_data.main.text_color -%}
  {%- capture color_style -%} style="color:{{ project_data.main.text_color }};" {%-endcapture-%}
{%- endif %}
  <h1 {{ color_style }}>{{ project_data.main.header | default: "Projects" }}</h1>
  <p {{ color_style }}>{{ project_data.main.info | default: "No data, check page_data in [language]/tabs/projects.md front matter or _data/content/projects/[language].yml" }}</p>
  <div class="multipurpose-button-wrapper">
  {% for category in project_data.category %}
    <a href="#{{ category.type }}" role="button" aria-pressed="false" data-project-filter="{{ category.type }}" class="multipurpose-button project-buttons" style="background-color:{{ category.color }};">{{ category.title }}</a>
  {% endfor %}
  </div>
</div>

{% for category in project_data.category -%}
  {%- capture first_category_id -%} id="{{ category.type }}" {%-endcapture-%}
  {% for list in project_data.list -%}
    {%- if list.type != category.type %}{% continue %}{% endif -%}
    <div class="multipurpose-container project-container" data-project-category="{{ category.type }}" {{ first_category_id }}>
      {%-assign first_category_id=nil -%}
      {%- include multi_lng/get-localized-long-date-format.liquid date = list.date -%}
      <div class="row">
        {% if list.img %}
          {%- assign prj_img_path = list.img -%}
          {%- assign prj_img_title = list.img_title -%}
        {% elsif site.data.conf.others.projects.project_img_fill %}
          {%- assign prj_img_path = "/assets/img/default/1x1px.png" -%}
          {%- assign prj_img_title = "" -%}
        {% endif %}
        {% if list.img or site.data.conf.others.projects.project_img_fill -%}
        <div class="col-md-3 project-img">
          <img src="{{ prj_img_path }}" alt="{{ prj_img_title }}">
        </div>
        {%- endif %}
        <div class="col-md-9 project-header">
          <h1>{{ list.project_name }}</h1><h2>{{ list.project_excerpt }}</h2>
          <div class="meta-container">
            <p class="date"><i class="fa fa-calendar fa-fw" aria-hidden="true"></i>&nbsp;{{ list.date | date: out_date_format }}</p>
            <p class="category">#{{ category.title }}</p>
          </div>
          <hr>
          <a href="javascript:void(0);" class="read-more-less" role="button" rel="nofollow">
            <div class="read-more"><i class="fa fa-angle-double-down fa-fw" aria-hidden="true"></i>{{ site.data.lang[lng].projects.read_more_text }}</div>
            <div class="read-less"><i class="fa fa-angle-double-up fa-fw" aria-hidden="true"></i>{{ site.data.lang[lng].projects.read_less_text }}</div>
          </a>
        </div>
      </div>
      <div class="row">
        <div class="markdown-style">
          {{ list.post | markdownify }}
          <a href="javascript:void(0);" class="read-more-less" role="button" rel="nofollow">
            <i class="fa fa-angle-double-up fa-fw" aria-hidden="true"></i>{{ site.data.lang[lng].projects.read_less_text }}
          </a>
        </div>
      </div>
    </div>
  {%- endfor %}
{%- endfor %}

<script>
  /* 분류 버튼: 누르면 그 분류만 보이고, 같은 버튼을 다시 누르면 전체가 다시 보인다 (HTML 압축이 줄바꿈을 지우므로 // 주석 금지) */
  (function () {
    var buttons = document.querySelectorAll('[data-project-filter]');
    var cards = document.querySelectorAll('[data-project-category]');
    var active = null;
    function apply(type) {
      active = type;
      cards.forEach(function (card) {
        card.style.display = !type || card.getAttribute('data-project-category') === type ? '' : 'none';
      });
      buttons.forEach(function (btn) {
        var on = btn.getAttribute('data-project-filter') === type;
        btn.setAttribute('aria-pressed', on ? 'true' : 'false');
        btn.style.opacity = type && !on ? '0.5' : '';
      });
    }
    buttons.forEach(function (btn) {
      btn.addEventListener('click', function (e) {
        e.preventDefault();
        var type = btn.getAttribute('data-project-filter');
        apply(active === type ? null : type);
      });
    });
    var start = location.hash.replace('#', '');
    if (document.querySelector('[data-project-filter="' + start + '"]')) apply(start);
  })();
</script>

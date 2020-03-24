---
layout: page
title: 是英语
titlebar: english
subtitle: <span class="mega-oction oction-clippy"></span>&nbsp;&nbsp;在学英语
menu: python
css: ['blog-page.css']
permalink: /english
---

<div class="row">
   
   <div class="col-md-12">
        
        <ul id="posts-list">
             {% for post in site.posts %}
                 {% if post.category=='english' or post.keywords contains 'english' %}
                 <li class="posts-list-item">
                     <div class="posts-content">
                          <span class="posts-list-meta">{{ post.date | date: "%Y-%m-%d" }}</span>
                          <a class="posts-list-name bubble-float-left" href="{{ site.url }}{{ post.url }}">{{ post.title }}</a>
                        <span class='circle'></span>
                    </div>
                </li>
                {% endif %}
            {% endfor %}
        </ul> 

        <!-- Pagination -->
        {% include pagination.html %}

        <!-- Comments -->
       <div class="comment">
         {% include comments.html %}
       </div>
    </div>

</div>
<script>
    $(document).ready(function(){

        // Enable bootstrap tooltip
        $("body").tooltip({ selector: '[data-toggle=tooltip]' });

    });
</script>

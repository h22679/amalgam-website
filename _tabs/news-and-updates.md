---
layout: page
icon: fas fa-bullhorn
order: 1
---

<div id="post-list" class="flex-grow-1 px-xl-1">
  {% assign sorted_announcements = site.announcements | sort: 'date' | reverse %}
  {% for announcement in sorted_announcements %}
    <article class="card-wrapper card">
      <a href="{{ announcement.url | relative_url }}" class="post-preview row g-0 flex-md-row-reverse">
        <div class="col-md-12">
          <div class="card-body d-flex flex-column">
            <h1 class="card-title my-2 mt-md-0">{{ announcement.title }}</h1>
            <div class="card-text content mt-0 mb-3">
              <p>{{ announcement.content | strip_html | truncatewords: 50 }}</p>
            </div>
            <div class="post-meta flex-grow-1 d-flex align-items-end">
              <div class="me-auto">
                <i class="far fa-calendar fa-fw me-1"></i>
                <time data-ts="{{ announcement.date | date: '%s' }}" data-df="ll">
                  {{ announcement.date | date: "%b %d, %Y" }}
                </time>
                <!-- If categories are used in announcements -->
                {% if announcement.categories %}
                  <i class="far fa-folder-open fa-fw me-1"></i>
                  <span class="categories">
                    {% for category in announcement.categories %}
                      {{ category }}
                    {% endfor %}
                  </span>
                {% endif %}
              </div>
            </div>
            <!-- .post-meta -->
          </div>
          <!-- .card-body -->
        </div>
      </a>
    </article>
  {% endfor %}
</div>

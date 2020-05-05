---
layout: page 
title: S106 Perpetuity and Nominations audit 
---

 <div class="album py-5 bg-light">
    <div class="container">

      <div class="row">
{% for scheme in site.data.s106list %}
        <div class="col-md-4">
          <div class="card mb-4 shadow-sm">
            <img class="card-img-top" src="{{ scheme.image_path }}" alt="{{ scheme.name }}">
            <div class="card-body">
              <p class="card-text">{{ scheme.comment }}</p>
              <div class="d-flex justify-content-between align-items-center">
                <div class="btn-group">
                  <a href="{{ scheme.url }}">
                  <button type="button" class="btn btn-sm btn-outline-secondary">View S106</button>
                  </a>
                </div>
                <small class="text-muted">9 mins</small>
              </div>
            </div>
          </div>
        </div>
{% endfor %}
  </div>
</div>
</div>


---
permalink: /about/
title: "About"
#excerpt: "About us."
last_modified_at: 2020-11-24
author_profile: true
header:
  overlay_image: "/assets/images/about.jpg"
  overlay_filter: 0.50
---

This is our personal blog, where we like to talk about our career and technologies we are passionate about.
{: .text-justify}

## Who we are

We are passionate about technology and we want to share what we know with you. Our career is mostly around Microsoft stack, but we promisse not to bore everybody with only that.
{: .text-justify}

## Skills

- Azure
- AWS
- GCP
- Terraform
- Packer
- Vagrant
- Docker
- Kubernetes
- Infrastructure as Code
- Continuous Integration
- Continuous Delivery
- Continuous Deployment
- Automation
- Pipelines

## Contacts

<div class="container">
  <p></p>
</div>

<!-- ALEX GIANNOTTI -->
{% assign author_alex = site.data.authors["Alex Giannotti"] %}

<div itemscope itemtype="https://schema.org/Person">

  {% if author_alex.avatar %}
    <div class="author__avatar">
      {% if author_alex.home %}
        <a href="{{ author_alex.home | relative_url }}">
          <img src="{{ author_alex.avatar | relative_url }}" alt="{{ author_alex.name }}" itemprop="image">
        </a>
      {% else %}
        <img src="{{ author_alex.avatar | relative_url }}" alt="{{ author_alex.name }}" itemprop="image">
      {% endif %}
    </div>
  {% endif %}

  <div class="author__content">
    {% if author.home %}
      <a href="{{ author_alex.home | relative_url }}"><h3 class="author__name" itemprop="name">{{ author_alex.name }}</h3></a>
    {% else %}
      <h3 class="author__name" itemprop="name">{{ author_alex.name }}</h3>
    {% endif %}
  </div>

  <div class="author__urls-wrapper">
    <button class="btn btn--inverse">{{ site.data.ui-text[site.locale].follow_label | remove: ":" | default: "Follow" }}</button>
    <ul class="author__urls social-icons">
      {% if author_alex.location %}
        <li itemprop="homeLocation" itemscope itemtype="https://schema.org/Place">
          <i class="fas fa-fw fa-map-marker-alt" aria-hidden="true"></i> <span itemprop="name">{{ author_alex.location }}</span>
        </li>
      {% endif %}

      {% if author_alex.links %}
        {% for link in author_alex.links %}
          {% if link.label and link.url %}
            <li><a href="{{ link.url }}" rel="nofollow noopener noreferrer"><i class="{{ link.icon | default: 'fas fa-link' }}" aria-hidden="true"></i><span class="label">{{ link.label }}</span></a></li>
          {% endif %}
        {% endfor %}
      {% endif %}

      {% if author_alex.uri %}
        <li>
          <a href="{{ author_alex.uri }}" itemprop="url">
            <i class="fas fa-fw fa-link" aria-hidden="true"></i><span class="label">{{ site.data.ui-text[site.locale].website_label | default: "Website" }}</span>
          </a>
        </li>
      {% endif %}

      {% if author_alex.linkedin %}
        <li>
          <a href="https://www.linkedin.com/in/{{ author_alex.linkedin }}" itemprop="sameAs" rel="nofollow noopener noreferrer">
            <i class="fab fa-fw fa-linkedin" aria-hidden="true"></i><span class="label">LinkedIn</span>
          </a>
        </li>
      {% endif %}

      {% if author_alex.github %}
        <li>
          <a href="https://github.com/{{ author_alex.github }}" itemprop="sameAs" rel="nofollow noopener noreferrer">
            <i class="fab fa-fw fa-github" aria-hidden="true"></i><span class="label">GitHub</span>
          </a>
        </li>
      {% endif %}

      {% include author-profile-custom-links.html %}
    </ul>
  </div>
</div>

<div class="container">
  <p></p>
</div>

<!-- MAX FERNANDES -->
{% assign author_max = site.data.authors["Max Fernandes"] %}

<div itemscope itemtype="https://schema.org/Person">

  {% if author_max.avatar %}
    <div class="author__avatar">
      {% if author_max.home %}
        <a href="{{ author_max.home | relative_url }}">
          <img src="{{ author_max.avatar | relative_url }}" alt="{{ author_max.name }}" itemprop="image">
        </a>
      {% else %}
        <img src="{{ author_max.avatar | relative_url }}" alt="{{ author_max.name }}" itemprop="image">
      {% endif %}
    </div>
  {% endif %}

  <div class="author__content">
    {% if author.home %}
      <a href="{{ author_max.home | relative_url }}"><h3 class="author__name" itemprop="name">{{ author_max.name }}</h3></a>
    {% else %}
      <h3 class="author__name" itemprop="name">{{ author_max.name }}</h3>
    {% endif %}
  </div>

  <div class="author__urls-wrapper">
    <button class="btn btn--inverse">{{ site.data.ui-text[site.locale].follow_label | remove: ":" | default: "Follow" }}</button>
    <ul class="author__urls social-icons">
      {% if author_max.location %}
        <li itemprop="homeLocation" itemscope itemtype="https://schema.org/Place">
          <i class="fas fa-fw fa-map-marker-alt" aria-hidden="true"></i> <span itemprop="name">{{ author_max.location }}</span>
        </li>
      {% endif %}

      {% if author_max.links %}
        {% for link in author_max.links %}
          {% if link.label and link.url %}
            <li><a href="{{ link.url }}" rel="nofollow noopener noreferrer"><i class="{{ link.icon | default: 'fas fa-link' }}" aria-hidden="true"></i><span class="label">{{ link.label }}</span></a></li>
          {% endif %}
        {% endfor %}
      {% endif %}

      {% if author_max.uri %}
        <li>
          <a href="{{ author_max.uri }}" itemprop="url">
            <i class="fas fa-fw fa-link" aria-hidden="true"></i><span class="label">{{ site.data.ui-text[site.locale].website_label | default: "Website" }}</span>
          </a>
        </li>
      {% endif %}

      {% if author_max.linkedin %}
        <li>
          <a href="https://www.linkedin.com/in/{{ author_max.linkedin }}" itemprop="sameAs" rel="nofollow noopener noreferrer">
            <i class="fab fa-fw fa-linkedin" aria-hidden="true"></i><span class="label">LinkedIn</span>
          </a>
        </li>
      {% endif %}

      {% if author_max.github %}
        <li>
          <a href="https://github.com/{{ author_max.github }}" itemprop="sameAs" rel="nofollow noopener noreferrer">
            <i class="fab fa-fw fa-github" aria-hidden="true"></i><span class="label">GitHub</span>
          </a>
        </li>
      {% endif %}

      {% include author-profile-custom-links.html %}
    </ul>
  </div>
</div>

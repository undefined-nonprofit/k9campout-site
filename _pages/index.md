---
layout: splash
author_profile: false
description: "Welcome to K9 Campout - a human pup and handler event at TRC, operated by Undefined"
permalink: /
header:
  image: /assets/images/k9campout_banner.jpg
---

K9 Campout is a human pup and handler event proudly operated by **[Undefined](http://undefined.charity)**. The event is for LGBTQ+ people who enjoy human pups and those who love them. 2025 marks the fourth year in a row for this amazing community gathering - and we look forward to seeing you all at TRC, August 15-17!

As a registered non-profit, we're committed to keeping costs low, maintaining transparency, and creating an inclusive, safe space for all attendees.

**Join our community:** [Telegram Channel](/telegram)

<script async src="https://telegram.org/js/telegram-widget.js?22" data-telegram-post="k9campout/110" data-width="100%"></script>

<h3 class="archive__subtitle">{{ site.data.ui-text[site.locale].recent_posts | default: "Recent Posts" }}</h3>

{% if paginator %}
  {% assign posts = paginator.posts %}
{% else %}
  {% assign posts = site.posts %}
{% endif %}

{% assign entries_layout = page.entries_layout | default: 'list' %}
<div class="entries-{{ entries_layout }}">
  {% for post in posts limit:3 %}
    {% include archive-single.html type=entries_layout %}
  {% endfor %}
</div>

{% include paginator.html %}

---
layout: default
title: Linux Kernel Contributions
permalink: /linux/
---

<style>
  .page-header { display: none !important; }
  .main-content { padding-top: 5rem !important; position: relative; }
  .lang-switcher {
    position: absolute;
    top: 1.5rem;
    right: 0;
    font-size: 1.1rem !important;
    color: #24292e !important;
    z-index: 999;
  }
  .lang-switcher a {
    color: #159957 !important;
    text-decoration: none !important;
    font-weight: bold;
  }
  .lang-switcher a:hover {
    text-decoration: underline !important;
  }
</style>

# Linux Kernel Contributions

Upstream contributions to the Linux kernel.

Author: jaedon.shin@gmail.com

Total Commits: {{ site.data.linux | size }}

---

{% assign commits = site.data.linux | sort: "date" | reverse %}
{% assign current_year = "" %}

{% for commit in commits %}
  {% assign year = commit.date | slice: 0, 4 %}

  {% if year != current_year %}
    {% assign current_year = year %}

## {{ year }}
  {% endif %}

- {{ commit.subject }}


  {{ commit.date }} ·
  <a href="https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id={{ commit.sha }}" target="_blank">{{ commit.sha | slice: 0, 12 }}</a>


{% endfor %}

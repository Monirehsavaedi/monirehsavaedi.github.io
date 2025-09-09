---
layout: default
title: خانه
---

<link rel="stylesheet" href="{{ '/assets/css/custom.css' | relative_url }}">

# Monireh Savaedi (PersianCruella) 👋
من **منیره سواعدی** هستم؛ درباره‌ی **امنیت سایبری، شبکه و کلود** می‌نویسم.  
این صفحه معرفی کوتاه منه و پایین، نوشته‌های بلاگ رو می‌بینید.

---

## دربارهٔ من
- علاقه‌مند به امنیت، شبکه و رایانش ابری
- تولید محتوا و مستندسازی فنی
- اشتراک تجربه‌ها و مسیر یادگیری

<div style="margin:16px 0;">
  <a class="btn" href="mailto:{{ site.email | default: 'you@example.com' }}">ایمیل</a>
  <a class="btn" href="{{ site.linkedin_url | default: '#' }}" target="_blank" rel="noopener">LinkedIn</a>
  <a class="btn" href="https://github.com/{{ site.github_username }}" target="_blank" rel="noopener">GitHub</a>
</div>

---

## مهارت‌ها
- Linux • Networking (TCP/IP, DNS, VPN)
- Cloud basics (IaaS/PaaS) • Git/GitHub
- Security basics (TLS, Hardening, Zero Trust)

---

<a id="blog"></a>
# بلاگ

{% assign posts_exist = site.posts | size %}
{% if posts_exist == 0 %}
هنوز پستی منتشر نشده است. اولین پست را در پوشه‌ی `_posts` بسازید 🙂
{% else %}
<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <small> – {{ post.date | date: "%Y-%m-%d" }}</small>
      {% if post.excerpt %}<br><span style="opacity:.8">{{ post.excerpt | strip_html | truncate: 160 }}</span>{% endif %}
    </li>
  {% endfor %}
</ul>
{% endif %}

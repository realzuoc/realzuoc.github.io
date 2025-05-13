---
permalink: /
title: ""
excerpt: ""
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

{% if site.google_scholar_stats_use_cdn %}
{% assign gsDataBaseUrl = "https://cdn.jsdelivr.net/gh/" | append: site.repository | append: "@" %}
{% else %}
{% assign gsDataBaseUrl = "https://raw.githubusercontent.com/" | append: site.repository | append: "/" %}
{% endif %}
{% assign url = gsDataBaseUrl | append: "google-scholar-stats/gs_data_shieldsio.json" %}

<span class='anchor' id='about-me'></span>

I am Chen Zuo (左 晨), a doctoral candidate in the [Optical Wireless Power Transmission (OWPT) Laboratory](http://vcsel-www.pi.titech.ac.jp/index-j.html) at the [Institute of Science Tokyo](https://www.isct.ac.jp/en), advised by [Prof. Tomoyuki Miyamoto](https://www.first.iir.titech.ac.jp/member/core3/#miyamoto).
Our research for OWPT is mainly construction of close-range indoor and long-range outdoor OWPT, this system integration work contains VCSEL beam-shaping, and automatic laser-emission regulation, uniting optical design, semiconductor physics, and computer-vision-driven control.
Take a glance at the [OWPT technology here!](https://youtu.be/pdI2E4NjI8s?si=lOi6FKB9_znatIfj)

Since 2022 I have also been a research assistant at FIRST, Institute of Innovative Research (IIR), where me and lab members did prototype IoT-enabled OWPT system and the closed-loop control&tracking towards power receiving target.

**Research Interest** Currently, we are focusing on Camera based safety system for OWPT, a method will lead to new standard for Laser Safety, *Automatic Emission Control(AEC)*.
This includes [Beam Tracking](http://dx.doi.org/10.1109/ACCESS.2025.3542769), [Shaping](https://doi.org/10.3390/en18092310), Beam Control, Object Recognition and more. More specific topics:

- Performance and evaluation of OWPT system in mid to long distance OWPT.
- Laser power converter performance assessment and optics design for various applications.
- OWPT safety related: using sensors or cameras to fulfill AEC for safety of laser devices.

Outside the lab, I enjoy hiking and photography—occasional snapshots and trip logs appear on my blog.

# 🔥 News

- _[2025.04]_: &nbsp;🎉🎉 Awarded with **Student Paper Award** on The 7th Optical Wireless and Fiber Power Transmission Conference!

# 📸 Photograph Blog

{% assign recent = site.posts | slice: 0, 3 %}

<section id="recent-posts">
  <h2>Recent posts</h2>
  <ul>
    {% for post in recent %}
      <li>
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        <span class="date">{{ post.date | date: "%b %d, %Y" }}</span>
      </li>
    {% endfor %}
  </ul>

<a class="btn btn-sm" href="{{ '/blog/' | relative_url }}">See all&nbsp;posts →</a>

</section>

# 📝 Publications

## Journal Papers

- [Camera-Based Safety System for Optical Wireless Power Transmission Using Dynamic Safety-Distance](https://www.mdpi.com/2304-6732/11/6/500)  
  Chen Zuo, Tomoyuki Miyamoto  
  *MDPI Photonics*

## Conferences

- [Advanced OWPT Safety System: Improved Metrics and Optimization for Multiple Intrusion Objects](https://pub.confit.atlas.jp/ja/event/opic2025/presentation/OWPT2-02)  
  Chen Zuo, Tomoyuki Miyamoto  
  *OWPT2025*
- 3D-Camera Based Optical Wireless Power Transmission Safety System for Light Beam Scanning Applications  
  Chen Zuo, Tomoyuki Miyamoto  
  *MOC2024*
- [Integrative Dynamic Safety System for OWPT: Real-Time Velocity and Distance-Based Safety Control](https://confit.atlas.jp/guide/event/opic2024/subject/OWPT6-02/detail)  
  Chen Zuo, Tomoyuki Miyamoto  
  *OWPT2024*
- [Improvement of Optical Wireless Power Transmission Safety System Using Depth Camera by New Safety Distance](https://confit.atlas.jp/guide/event/opic2023/subject/OWPT11-05/crosssearch)  
  Chen Zuo, Tomoyuki Miyamoto  
  *OWPT2023*

# 🎖 Honors and Awards

- _2025_ Student Paper Award — OWPT 2025
- _2023_ [Student Paper Award — OWPT 2023](https://www.first.iir.titech.ac.jp/detail_1455/)
- _2023_ [Outstanding Master Student Award — Institute of Science Tokyo 2023](https://educ.titech.ac.jp/ee/eng/news/2024_04/065884.html)
- _2021_ Excellent Undergraduate Thesis — Suzhou University of Technology 2021
- University Scholarship (Second) — 2021
- University Scholarship (Second) — 2020
- University Scholarship (First) — 2019
- Excellent AIESEC Global Volunteer — 2018

# 📖 Educations

- **Oct 2023 – Present** | Ph.D.(Eng.), Institute of Science Tokyo | _Advanced OWPT Safety System toward Error-Free Safety_ |
- **Nov 2021 – Jul 2023** | M.Eng., Institute of Science Tokyo | _Fundamental Investigation of Camera-Based Safety System of OWPT_ |
- **Sep 2017 – Jun 2021** | B.Eng., Suzhou University of Technology | _Mode Characteristics Analysis of the Ridged Waveguide_ |<!-- :contentReference[oaicite:6]{index=6}:contentReference[oaicite:7]{index=7} -->

[//]: # "# 💬 Invited Talks"
[//]: # "- *2021.06*, Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus ornare aliquet ipsum, ac tempus justo dapibus sit amet. "
[//]: # "- *2021.03*, Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus ornare aliquet ipsum, ac tempus justo dapibus sit amet.  | [[video]](https://github.com/)"

# 💻 Internships

- _2022.05 - Present_, Research Assistant, FIRST, IIR, Institute of Science Tokyo, Japan.

---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

PDF format
======
You can download my CV in PDF format [here](https://lrobidou.github.io/files/CV.pdf)

Education
======
* Prep school at Lycée Lesage, in Vannes, 2015 - 2017
* Engineering school (computer science) at Sup Galilée, in Villetaneuse, 2017 - 2020
  * university exchange program, at Hanyang University, in Seoul (one semester)
* Ph.D at Inria, in Rennes, 2020 - 2023 (expected)

Work experience
======
* 2020-2023: PhD student
  * Inria, Rennes (Britanny)
  * Supervisor: Pierre Peterlongo

* 2020: Internship - Software engineer
  * Sopra Steria, St Gregoire (Britanny)
  * Duties included: discussion with the client, documentation, tests, development, code reviews...

* 2019: Internship - Software developer
  * National center for scientific research (CNRS), Villetaneuse (Île-de-France)
  * Duties included: discussion with the client, documentation, development...
  * tech used: Python

* 2018 - 2019: group project
  * National center for scientific research (CNRS), Villetaneuse (Île-de-France)
  * Creation of a website to plot chemical reactions graphs [https://ammonx.lspm.cnrs.fr/](https://ammonx.lspm.cnrs.fr/)
  * tech used: PHP

Skills
======
* programming languages
  * Python
  * C++
  * Rust
  * Java
  * C
  * ...

Publications
======
  <ul>{% for post in site.publications %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
Talks
======
  <ul>{% for post in site.talks %}
    {% include archive-single-talk-cv.html %}
  {% endfor %}</ul>
  
Teaching
======
  <ul>{% for post in site.teaching %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>

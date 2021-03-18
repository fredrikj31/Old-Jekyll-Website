---
layout: splash
author: "Fredrik Johansen"
classes: wide

header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/images/landscape.jpg
  caption: "Photo credit: [**Wall Alphacoders**](https://wall.alphacoders.com/big.php?i=102609)"
excerpt: "Welcome to my website. Here you can find some of the projects that I have over the last couple of years. Here I also host my blog, where you can learn some of the things that I have learned so far."


projects:
  - image_path: https://wallpaperaccess.com/full/170249.jpg
    alt: "placeholder image 1"
    title: "Placeholder 1"
    excerpt: "This is some sample content that goes here with **Markdown** formatting."
    url: "/portfolio/testProject1/"
    btn_label: "Read More"
    btn_class: "btn--inverse"
  - image_path: https://i.pinimg.com/originals/3e/2a/f6/3e2af664e061013a3d05aa99fa20c1d4.jpg
    alt: "placeholder image 2"
    title: "Placeholder 2"
    excerpt: "This is some sample content that goes here with **Markdown** formatting."
    url: "/portfolio/testProject1/"
    btn_label: "Read More"
    btn_class: "btn--inverse"
  - image_path: https://wallpapercave.com/wp/XMnhQSq.jpg
    title: "Placeholder 3"
    excerpt: "This is some sample content that goes here with **Markdown** formatting."
    url: "/portfolio/testProject1/"
    btn_label: "Read More"
    btn_class: "btn--inverse"

---

{% assign todayDateHej = "2021-06-11" %}

{% assign currentYear = todayDateHej | date: "%Y" %}
{% assign birthdayYear = "2003-06-12" | date: "%Y" %}

{% assign currentMonth = todayDateHej | date: "%m" %}
{% assign birthdayMonth = "2003-06-12" | date: "%m" %}

{% assign currentDay = todayDateHej | date: "%d" %}
{% assign birthdayDay = "2003-06-12" | date: "%d" %}

<!-- Checking if birthday month is greater than current month -->
{% if currentMonth > birthdayMonth %}
{{ assign age = currentYear | minus: birthdayYear }}
{% elsif currentMonth == birthdayMonth %}
{% if currentDay > birthdayDay %}
{{ assign age = currentYear | minus: birthdayYear }}
{% elsif currentDay == birthdayDay %}
{{ assign age = currentYear | minus: birthdayYear }}
{% else %}
{{ assign age = currentYear | minus: birthdayYear | minus: 1 }}
{% endif %}
{% else %}
{{ assign age = currentYear | minus: birthdayYear | minus: 1 }}
{% endif %}

<h1>Welcome to my website!</h1>
<img src="https://avatars.githubusercontent.com/u/31306224?s=460&u=d3bf0bdd7b29cc137a3c74472b32726a41c8b8e7&v=4" width="200" height="200" style="border-radius: 50%;" />{: .align-right}
Fredrik Johansen is a {{ age }} years old software developer who likes to learn and teach code. He writes blog posts about his new findings and code-related things.
This is my website hosted on proudly hosted on Github. But as said I like to teach other people coding, because I think coding will be the magic of the future. Follow my social medias, where I will post coding-related stuff.

<br>

# Featured Projects

{% include feature_row id="projects" %}

# Testimonials

[//]: # "First Testimonial"
**John Doe** - Software Developer at Google
<img src="https://www.homeandhelp.com/img/pages/32/a3a42e4e9d84f01cd08d0832682ab694.jpg" width="150" height="150" style="border-radius: 50%;" />{: .align-right}

*"Fredrik Johansen is a very talented programmer, who codes every project to the clients liking. Fredrik does not compromise the details of the project even if he need 10 more hours to make it done."*

<br>

[//]: # "Second Testimonial"
**John Doe** - Software Developer at Google
<img src="https://images.squarespace-cdn.com/content/v1/5bce1ed034c4e2d741fe15fc/1542058813138-D0CYK18TQXAAOBAJ1JVG/ke17ZwdGBToddI8pDm48kP06O0_IHyRXSOOiqwgWaApZw-zPPgdn4jUwVcJE1ZvWEtT5uBSRWt4vQZAgTJucoTqqXjS3CfNDSuuf31e0tVEHLRkg2cosQUGLeQ33UzXdgIxPDaVwE3LlEpL74qP4JVW4jCyXLPvvdR287iymYt8/Female_Blank_Avatar.jpg" width="150" height="150" style="border-radius: 50%;" />{: .align-left}

*"Fredrik Johansen is a very talented programmer, who codes every project to the clients liking. Fredrik does not compromise the details of the project even if he need 10 more hours to make it done."*

<br>
<hr>

# Latest Blog Posts

{% include_relative /assets/components/latestPosts.html %}

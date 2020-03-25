---
permalink: /encryption/
#title: "Introduction."
excerpt: "Password Protection information"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

The static pages password protection technique uses a SHA-1 encrypted password, generated using a randomised password generator. The SHA-1 hash is then made the title of the root folder for the website, and is placed in parallel with the index.html file containing the login screen. Upon entering the password, index.html checks the SHA-1 alongside the title of the root folder and if it matches, changes up to that directory.

The problem is, the index.html file then looks for another index.html file inside the root directory to display as the main web page. The academic pages Jekyll site I am using does not contain an index.html homepage so upon pushing this via github desktop, I recieve build errors.
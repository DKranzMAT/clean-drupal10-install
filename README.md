FA Demo — Drupal 10 Custom Theme
A lightweight, interview-ready Drupal 10 demo theme inspired by Feeding America’s clean, nonprofit aesthetic. Built to showcase component-driven front-end structure, modular Twig templates, and a focus on UX clarity.
🧩 Theme Highlights
•	Custom page.html.twig layout (no base theme dependency)
•	Hero section with flexible gradient banner and call-to-action buttons
•	“Impact strip” and “Ways to Help” sections styled with accessible color contrast
•	Responsive flex/grid layout powered by modern CSS variables
•	Fully self-contained under web/themes/custom/fa_demo/
🗂️ File Structure
fa_demo/ ├── css/ │   └── style.css ├── templates/ │   └── page.html.twig ├── fa_demo.info.yml └── fa_demo.libraries.yml
⚙️ Setup
1.	Copy fa_demo into your Drupal project at:
web/themes/custom/fa_demo/
2.	Rebuild caches:
drush cr
3.	Enable and set the theme as default:
drush theme:enable fa_demo drush config:set system.theme default fa_demo -y
🎨 Color Palette
Token

Hex

Usage

--fa-green

#2e6e3b

Primary brand

--fa-orange

#f7941d

Accent buttons

--fa-cream

#fff7ec

Page background

--fa-sand

#f2e3cf

Section panels

--fa-text

#163018

Headlines & body


📄 Description
This minimalist one-page Drupal theme mimics a modern nonprofit landing page — blending purpose, clarity, and a real-world visual language that aligns with Feeding America’s approachable design ethos.
—————
Author: David Kranz Repo: clean-drupal10-install

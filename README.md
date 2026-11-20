<!-- ================= HEADER ================= -->

<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=700&size=27&duration=3000&pause=1000&color=00FF7F&center=true&vCenter=true&width=800&lines=Hi%2C+I'm+Yash+Jha+%F0%9F%91%8B;MCA+Student+%7C+Software+Developer;Full+Stack+Development+Enthusiast;Building+Ideas+Into+Reality!" alt="Typing SVG" />

<h3>💻 Aspiring Software Developer | MCA Student | Tech Enthusiast</h3>

<img src="https://komarev.com/ghpvc/?username=yashjha140&label=PROFILE+VIEWS&color=00FF7F&style=for-the-badge" alt="Profile views"/>

<a href="https://github.com/yashjha140">
<img src="https://img.shields.io/github/followers/yashjha140?label=Followers&style=for-the-badge&color=00FF7F&logo=github" alt="Followers"/>
</a>

</div>

---

<!-- ================= ABOUT ================= -->

## 🟢 About Me

Hello! I'm **Yash Jha**, an MCA student passionate about technology, programming and software development.

- 🎓 Pursuing MCA at **VIPS, GGSIPU (2025–2027)**
- 🎓 BCA Graduate from GGSIPU (2025)
- 💻 Interested in Full Stack Development and Software Engineering
- 🌱 Currently strengthening my programming and problem-solving skills
- 🚀 Building practical projects and exploring new technologies
- 🎯 Aspiring to become a professional software developer

---

<!-- ================= TECH STACK ================= -->

## 🛠️ Tech Stack & Technologies

### Programming Languages

<p>
<img src="https://skillicons.dev/icons?i=c,python,js" />
</p>

### Web Development

<p>
<img src="https://skillicons.dev/icons?i=html,css" />
</p>

### Database & Development Tools

<p>
<img src="https://skillicons.dev/icons?i=mysql,git,github,vscode" />
</p>

---

<!-- ================= PROJECTS ================= -->

## 🚀 Featured Projects

<table>
<tr>
<td width="50%">
<h3 align="center">🎓 EduPro AI</h3>
<div align="center">
<a href="https://github.com/yashjha140/EduPro-AI">
<img src="https://github-readme-stats.vercel.app/api/pin/?username=yashjha140&repo=EduPro-AI&theme=merko&hide_border=true" alt="EduPro AI repository card"/>
</a>
<p>Educational software project focused on improving educational processes.</p>
</div>
</td>
<td width="50%">
<h3 align="center">💡 More Projects Coming Soon</h3>
<div align="center">
<img src="https://img.shields.io/badge/Building-My_Next_Project-00FF7F?style=for-the-badge&logo=github&logoColor=black"/>

name: Generate Contribution Snake

on:
  schedule:
    - cron: "0 0 * * *"
  workflow_dispatch:
  push:
    branches:
      - main

permissions:
  contents: write

jobs:
  generate:
    runs-on: ubuntu-latest
    timeout-minutes: 10

    steps:
      - name: Generate snake animation
        uses: Platane/snk/svg-only@v3
        with:
          github_user_name: yashjha140
          outputs: |
            dist/github-contribution-grid-snake.svg
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark

      - name: Publish snake animation
        uses: crazy-max/ghaction-github-pages@v3.1.0
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

name: GitHub Profile 3D Contributions

on:
  schedule:
    - cron: "0 18 * * *"
  workflow_dispatch:

permissions:
  contents: write

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout repository
        uses: actions/checkout@v5

      - name: Generate 3D contribution calendar
        uses: yoshi389111/github-profile-3d-contrib@latest
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
          USERNAME: yashjha140

      - name: Commit generated images
        run: |
          git config user.name github-actions
          git config user.email github-actions@github.com
          git add -A .
          if git commit -m "Update 3D contribution calendar"; then
            git push
          fi

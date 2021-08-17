## Olá! Eu sou o Vitor Cabral!


- 🔭 Busco minha primeira oportunidade de trabalho.
- 🌱 Estudante de Engenharia da Computação - 2º semestre/ Faculdade Impacta.
- 🤓 Tenho interesse em back-end e engenharia de software.

 <div>
  <a href="https://github.com/Cabrauzz">
  <img height="180em" src="https://github-readme-stats.vercel.app/api?username=Cabrauzz&show_icons=false&theme=dark&include_all_commits=true&count_private=true"/>
  <img height="180em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Cabrauzz&layout=compact&langs_count=7&theme=dark"/>
</div>
<div style="display: inline_block"><br>
  <img align="center" alt="Vitor-Python" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg">
</div>
  
##
  <div>
    <a href="https://www.linkedin.com/in/vitor-cabral-4569b8203/" target="_blank"><img src="https://img.shields.io/badge/-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white" target="_blank"></a>

  </div>
 
 name: Generate Datas

on:
  schedule: # execute every 12 hours
    - cron: "* */12 * * *"
  workflow_dispatch:

jobs:
  build:
    name: Jobs to update datas
    runs-on: ubuntu-latest
    steps:
      # Snake Animation
      - uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: rafaballerini
          svg_out_path: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

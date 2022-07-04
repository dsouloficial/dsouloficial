
### ola! Eu sou Denilson Bernardo ✌️

<div align="center">
  <a href="https://github.com/dsouloficial">
    <img height="150em" src="https://github-readme-stats.vercel.app/api?username=dsouloficial&count_private=true&include_all_commits=true&show_icons=true&theme=dracula&hide_border=false&show_owner=true"/>
    <img height="150em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=dsouloficial&theme=dracula&hide_border=false&&layout=compact"/>


[![social](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://instagram.com/dsoul_oficial)
[![social](https://img.shields.io/badge/Twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://Twitter.com/dsouloficial)
[![social](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://Linkedln.com/DenilsonBernardo)


### tecnologias que eu uso no meu dia 

<div style="display: inline_block"><br/>
<img algin="center" alt= html5 src= https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white />
<img algin="center" alt= CSS src=https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white/>
<img algin="center" alt= Javascript src=https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black /> 
<img algin="center" alt= NODE.JS src= https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white/>

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
          github_user_name: dsouloficial
          svg_out_path: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

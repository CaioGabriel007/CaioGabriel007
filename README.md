## Hi there 👋
 <i>Eu sou o Caio Gabriel sou um programador Front End, tenho 19 anos e atualmente estou aprendendo :memo: e começando a criar projetos 💻 com:<i/>
 <br>
 <br>
   
   <img src="https://img.shields.io/badge/HTML-239120?style=for-the-badge&logo=html5&logoColor=white" />
   <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" />
   <br>
   <br>

   e aumentando o meu conhecimento para me tornar um <b>Full Stack.<br/>:muscle::smile:💻

  [![Caio Gabriel Stats](https://github-stats-extended.vercel.app/api?username=CaioGabriel007)](https://github.com/stats-organization/github-stats-extended)

name: Update README cards

on:
  schedule:
    - cron: "0 0 * * *" # Runs once daily at midnight
  workflow_dispatch:

jobs:
  build:
    runs-on: ubuntu-latest

    permissions:
      contents: write

    steps:
      - uses: actions/checkout@v6

      - name: Generate stats card
        uses: stats-organization/github-readme-stats-action@v2
        with:
          card: stats
          options: username=${{ github.repository_owner }}&show_icons=true
          path: profile/stats.svg
          token: ${{ secrets.GITHUB_TOKEN }}

      - name: Generate top languages card
        uses: stats-organization/github-readme-stats-action@v2
        with:
          card: top-langs
          options: username=${{ github.repository_owner }}&layout=compact&langs_count=6
          path: profile/top-langs.svg
          token: ${{ secrets.GITHUB_TOKEN }}

      - name: Generate pin card
        uses: stats-organization/github-readme-stats-action@v2
        with:
          card: pin
          options: username=stats-organization&repo=github-readme-stats
          path: profile/pin-stats-organization-github-readme-stats.svg
          token: ${{ secrets.GITHUB_TOKEN }}

      - name: Commit cards
        run: |
          git config user.name "github-actions[bot]"
          git config user.email "41898282+github-actions[bot]@users.noreply.github.com"
          git add profile/*.svg
          git commit -m "Update README cards" || exit 0
          git push
  <br>
  <br>
 <b>FATO CURIOSO:<b/>
 <br>
 <br>
 - Sempre dizia desde pequeno que eu gostaria de trabalhar com programação, e aos meus 18 anos deste ano antes de fazer aniversário; encontrei uma escola de programação online muito boa quando eu menos esperava, conhecida como DevClub, eu estava pensativo em que carreira seguir pois eu havia acabado de encerrar o ensino médio praticamente e acabei achando esta luz no final do túnel :sparkles:, e aqui estou eu, evoluindo dia após dia :smile_cat::rocket:

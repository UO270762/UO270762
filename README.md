### :alien: Hello to the people with the curse of software development :alien:


Several hours and nights have been spent on... :chart_with_upwards_trend:
<img src="https://github-readme-stats.vercel.app/api/top-langs?username=madushadhanushka&show_icons=true&locale=en&layout=compact&theme=chartreuse-dark" alt="ovi" />

![compu](https://i.kym-cdn.com/photos/images/newsfeed/002/086/808/90f.gif)

:snake:Have a break:snake:
![Snake animation](https://github.com/madushadhanushka/github-readme/blob/output/github-contribution-snake.svg)

name: Contribution snake

on:
  schedule: # execute every 12 hours
    - cron: "* */12 * * *"
  workflow_dispatch:

jobs:
  build:
    name: Jobs to update snake grid
    runs-on: ubuntu-latest
    steps:
      - uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: madushadhanushka
          svg_out_path: dist/github-contribution-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

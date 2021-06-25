# MAINTAINER [OIVAS7572](https://github.com/OIVAS7572)
[![Python](https://github.com/OIVAS7572/lichess-bot/actions/workflows/Python.yml/badge.svg)](https://github.com/OIVAS7572/lichess-bot/actions/workflows/Python.yml)
[![Docker](https://github.com/OIVAS7572/lichess-bot/actions/workflows/Docker.yml/badge.svg)](https://github.com/OIVAS7572/lichess-bot/actions/workflows/Docker.yml)

# lichess-bot
- A bridge between [Lichess API](https://lichess.org/api#tag/Bot) and bots.
- This bot is using Docker and is concentrated on Heroku server.

## How to Install on Heroku
- Import or [Fork](https://github.com/OIVAS7572/lichess-bot/fork) this repository to your Github.
- Open the `config.yml` file and insert API accses token in to token option and commit changes over [here](/config.yml#L1).
- Install [Heroku CLI](https://devcenter.heroku.com/articles/heroku-cli) and [create a new app](https://dashboard.heroku.com/new-app) in Heroku. <br/>
**Do note that in certain operating systems Heroku CLI doesn't get added to path automatically. If that's the case you'll have to add heroku to your path manually.**
- Run this command in cmd or powershell `heroku stack:set container -a appname`, where `appname` is replaced with your Heroku app's name.
- In heroku, in the `Deploy` tab click on `Connect to GitHub` and then click on `search` and select your fork/import of this repository.
- Now scroll down and under `Manual deploy`, click on `deploy` with the `master` branch selected. <br/>
**Do note that you could also `Enable Automatic Deploys` with the `master` branch selected if you would like each commit you make to get automatically and easily deployed onto your bot.**
- After deploying wait for about 5 minutes till the build finishes and then in the `Resources` tab in heroku turn `worker` dynos. If you do not see any option to enable any dynos, then you'll have to wait for about 5 minutes and then refresh your page on heroku.

You're now connected to lichess and awaiting challenges! Your bot is up and ready!

## INFO 
ENGINE:
- [Stockfish 13 SSE4.1 + POPCNT](https://stockfishchess.org/files/stockfish_13_linux_x64_modern.zip)

OPENING BOOKS: 
- [Goi5.1.bin](https://gitlab.com/OIVAS7572/Goi5.1.bin/-/raw/master/Goi5.1.bin.7z)
- [Drawkiller_EloZoom_big.bin](/Drawkiller_EloZoom_big.bin)

**If you want to run bot localy on PC, read the [lichess-bot manual](https://github.com/ShailChoksi/lichess-bot#how-to-install).**

## Acknowledgements
Credits to [ShailChoksi's lichess-bot](https://github.com/ShailChoksi/lichess-bot).

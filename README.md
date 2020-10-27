# What I've been working on

…this doesn't always acurately reflect the proportion of languages, but here's a rough idea:

<!--START_SECTION:waka-->
```text
Markdown     4 hrs 31 mins   ███████████▓░░░░░░░░░░░░░   46.67 % 
Python       4 hrs 9 mins    ██████████▓░░░░░░░░░░░░░░   42.88 % 
HTML         30 mins         █▒░░░░░░░░░░░░░░░░░░░░░░░   05.24 % 
INI          21 mins         █░░░░░░░░░░░░░░░░░░░░░░░░   03.66 % 
Git Config   8 mins          ▒░░░░░░░░░░░░░░░░░░░░░░░░   01.52 % 
```
<!--END_SECTION:waka-->

Instructions for the Wakatime readout above (see [the waka-readme repo](https://github.com/athul/waka-readme) and the [other page about this](https://github.com/marketplace/actions/waka-readme)) aren't really clear and seem to end with "That's it! The Action runs everyday at 00.00 UTC" which makes the rest of the text look optional.

---

## The code

```
name: Waka Readme

on:
  workflow_dispatch:
  schedule:
    # Runs at 12am UTC
    - cron: '0 0 * * *'

jobs:
  update-readme:
    name: Update this repo's README
    runs-on: ubuntu-latest
    steps:
      - uses: athul/waka-readme@master
        with:
          WAKATIME_API_KEY: ${{ secrets.WAKATIME_API_KEY }}
```

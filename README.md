# What I've been working on

…this doesn't always acurately reflect the proportion of languages, but here's a rough idea:

<!--START_SECTION:waka-->
```text
Python     11 hrs 16 mins  ████████████████▓░░░░░░░░   67.23 % 
Markdown   2 hrs 56 mins   ████▒░░░░░░░░░░░░░░░░░░░░   17.57 % 
Text       1 hr 38 mins    ██▒░░░░░░░░░░░░░░░░░░░░░░   09.74 % 
CSS        22 mins         ▓░░░░░░░░░░░░░░░░░░░░░░░░   02.25 % 
INI        8 mins          ▒░░░░░░░░░░░░░░░░░░░░░░░░   00.88 % 
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

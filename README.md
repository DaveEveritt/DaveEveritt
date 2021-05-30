# What I've been working on

…this doesn't always acurately reflect the proportion of languages, but here's a rough idea:

<!--START_SECTION:waka-->
```text
Markdown     4 hrs 53 mins   ████████▓░░░░░░░░░░░░░░░░   34.24 % 
JavaScript   3 hrs 50 mins   ██████▓░░░░░░░░░░░░░░░░░░   26.92 % 
HTML         2 hrs 28 mins   ████▒░░░░░░░░░░░░░░░░░░░░   17.34 % 
CSS          2 hrs 2 mins    ███▓░░░░░░░░░░░░░░░░░░░░░   14.32 % 
Text         23 mins         ▓░░░░░░░░░░░░░░░░░░░░░░░░   02.72 % 
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

# What I've been working on

…this doesn't always acurately reflect the proportion of languages, but here's a rough idea:

<!--START_SECTION:waka-->
```text
Markdown   2 hrs 24 mins   █████████████░░░░░░░░░░░░   52.07 % 
HTML       59 mins         █████▒░░░░░░░░░░░░░░░░░░░   21.57 % 
Ruby       58 mins         █████▒░░░░░░░░░░░░░░░░░░░   21.17 % 
CSS        11 mins         █░░░░░░░░░░░░░░░░░░░░░░░░   04.07 % 
JSON       3 mins          ▒░░░░░░░░░░░░░░░░░░░░░░░░   01.12 % 
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

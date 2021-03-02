# What I've been working on

…this doesn't always acurately reflect the proportion of languages, but here's a rough idea:

<!--START_SECTION:waka-->
```text
Perl       3 hrs 58 mins   ███████████░░░░░░░░░░░░░░   43.76 % 
Markdown   3 hrs 51 mins   ██████████▓░░░░░░░░░░░░░░   42.57 % 
Other      48 mins         ██▒░░░░░░░░░░░░░░░░░░░░░░   08.84 % 
HTML       26 mins         █▒░░░░░░░░░░░░░░░░░░░░░░░   04.83 % 
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

# What I've been working on

…alhough this doesn't always acurately reflect the proportion of languages, here's a rougn idea:

<!--START_SECTION:waka-->
<!--END_SECTION:waka-->

The Wakatime readout should be above - see [the waka-readme repo](https://github.com/athul/waka-readme) and the [other page about this](https://github.com/marketplace/actions/waka-readme) because the instructions aren't really clear and seem to end with

> That's it! The Action runs everyday at 00.00 UTC"

which makes the rest of the text look optional.

---

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

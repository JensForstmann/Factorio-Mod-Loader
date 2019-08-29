# Factorio-Mod-Loader
bash only, no other requirements

Downloads every enabled mod from the `mod-list.json`. Just that.

## Setup

Simply...

* copy the environment example file: `cp factorio-mod-loader.env.example factorio-mod-loader.env`
* change the three variables in `factorio-mod-loader.env`
* make the script executable: `chmod +x factorio-mod-loader.sh`
* run it: `./factorio-mod-loader.sh`

## Why? How?

**Q:** Why another mod downloader?

**A:** I wanted a script without any dependencies like python, ruby or jq.
After 5 minutes of searching and not finding anything I decided to hack a script together.

**Q:** Hack a script together?

**A:** Yeah, it is very quick and dirty. It doesn't really parse json.
It takes the json payload (both from the `mod-list.json` and the factorio mod api)
and `grep` and `sed` it multiple times to get it to a format it can download the mod zip files with `wget`.

## Soft Dependencies

* bash
* wget
* grep
* sed
* cat
* echo

So for a freshly installed ubuntu for example you won't need to install anything.

## Know Issues

* Potentially breaks if the json payload will change (because then the grep and sed part won't fit anymore).

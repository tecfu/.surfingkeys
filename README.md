# SurfingKeys Configuration

- Contents
  - Configuration Files
  - Instructions for Installation of [Hacked Plugin](https://github.com/tecfu/Surfingkeys) (Changed hardcoded coloring for hints)

## Motivation

SurfingKeys doesn't expose configuration to change the hint color. 

Guidance from the [README](https://github.com/brookhong/Surfingkeys/blob/master/docs/API.md#hintsstyle) simply doesn't work.

This hacked plugin changes [the hardcoded hint styling](https://github.com/tecfu/Surfingkeys/commit/0a0c2ca19789be350f0ecac739f6fae6c9a289ed).

### Background

I am using the [#enable-force-dark](https://superuser.com/questions/1484146/how-to-enforce-dark-mode-on-chrome-web-store) in chrome.
At the time of writing, this is the only way to convert chrome's internal pages (i.e. webstore, settings) to be in dark mode.

This README provides guidance on how to install the fork and accompanying configuration.

## Hacked Plugin Installation (SurfingKeys) (separate repo)

```
git clone https://github.com/tecfu/Surfingkeys
cd Surfingkeys
npm install
npm run build:prod
```

- Open the browser's extension page.
- For Chrome, this can be accessed through "chrome://extensions".
- Disable the Surfingkeys extension that was installed from the Google Chrome Store.
- Enable "Developer mode" then click "Load unpacked."
- Navigate to <pathToSurfingkeys>/dist/<env>/<browser>.

## SurfingKeys Configuration

- Extension > SurfingKeys > Details > Extension Options
- Enter contents of .surfingkeysrc or https://gist.githubusercontent.com/tecfu/87e5ce07e5c54cfbeed2198fe4f235af/raw/35ae65bec9eabb0c6bcc4f67b563904f75ea3207/.surfingkeysrc

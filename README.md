# SurfingKeys Configuration

## Motivation

Configuration docs for the chrome extension [Surfingkeys](https://github.com/brookhong/Surfingkeys).

I am using the [#enable-force-dark](https://superuser.com/questions/1484146/how-to-enforce-dark-mode-on-chrome-web-store) in chrome. At the time of writing, this is the only way to convert chrome's internal pages (i.e. webstore, settings) to be in dark mode. The #enable-force-dark flag doesn't play nicely with the hint boxes in SurfingKeys, so I had to [fork the plugin](https://github.com/tecfu/Surfingkeys/tree/hack_hint_sizes) and modify it.

This README provides guidance on how to install the fork and accompanying configuration.

## Surfingkeys Installation 

```
git clone https://github.com/tecfu/Surfingkeys
chd Surfingkeys
git checkout hack_hint_sizes
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

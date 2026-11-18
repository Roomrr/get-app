<p align="center">
  <img src="logo.png" alt="Roomrr" width="160" />
</p>

<h1 align="center">Get the Roomrr app</h1>

<p align="center">
  Find a room, and the people to share it with.
</p>

<p align="center">
  <a href="https://play.google.com/store/apps/details?id=com.roomrr.app"><b>Google Play</b></a>
  &nbsp;·&nbsp;
  <a href="https://apps.apple.com/in/app/roomrr/id6789584593"><b>App Store</b></a>
  &nbsp;·&nbsp;
  <a href="https://roomrr.com/"><b>roomrr.com</b></a>
</p>

---

## What this is

This is the page that opens when you scan a Roomrr QR code. It gets you to
the Roomrr app in one step:

| You open it on… | What happens |
| --- | --- |
| An Android phone | Google Play opens on the Roomrr app |
| An iPhone or iPad | The App Store opens on the Roomrr app |
| A computer or anything else | You stay on the page and choose Google Play, the App Store or the website |

If you came here looking for the app, use the links above.

## How it works

It's one static HTML page with no build step, no tracking scripts and no
cookies. A few lines of JavaScript read the browser's user agent and send
phones to the right store. Everything else sees the page with three buttons.

- iPads that identify themselves as a Mac are still recognised as iPads.
- Add `?stay` to the URL to see the page on a phone without being redirected.
- Google Play installs from this page are tagged `utm_source=qr` so QR
  downloads can be counted.
- The page follows the device's light or dark setting.

## Files

```
index.html          the page, with styles and script inline
logo.png            Roomrr logo
favicon-192.png     browser icon
fonts/              Manrope (medium, bold, extrabold)
```

The store and website links are in the `LINKS` object near the top of
`index.html`.

## Running it locally

Open `index.html` in a browser, or serve the folder:

```sh
python3 -m http.server 8080
```

Then visit <http://localhost:8080>. On a computer you'll stay on the page.
Open `http://localhost:8080/?stay` on a phone to see it there without the
redirect.

## Deploying

Upload the folder to any static host and point the QR code at its URL.

---

<p align="center">
  © Roomrr · <a href="https://roomrr.com/">roomrr.com</a>
</p>

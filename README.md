# User Agent Parser

Break a User-Agent string into browser, engine, operating system, and device type. No server, no tracking, no third-party scripts.

**Live demo:** https://0xelitesystem.github.io/user-agent-parser/

## Use

Open `index.html` in any modern browser, or visit the GitHub Pages link in the repo description.

Paste a User-Agent string, or click "Use my browser" to load the one your browser is sending. The tool parses it locally and shows:

- Browser name and version
- Operating system name and version
- Device type (Desktop, Mobile, Tablet, TV, or Bot or tool)
- Rendering engine and version (Blink, WebKit, Gecko, Trident, and others)

A full breakdown table lists every parsed field. It recognizes Chrome, Firefox, Safari, Edge, Opera, Samsung Internet, Brave, Vivaldi, Chromium, Internet Explorer, the iOS variants (CriOS, FxiOS), common command-line tools (curl, wget, python-requests), and well-known crawlers.

## Why this exists

Reading a raw User-Agent string by eye is error prone. The browser token order is misleading (Chrome pretends to be Safari, Edge pretends to be Chrome), and OS versions are encoded oddly (Windows NT 10.0, `10_15_7`). Most parsers ship as a dependency you have to install, or run on a server that logs what you send. This is a single page that parses everything with local heuristics and makes no network calls.

Heads up: User-Agent strings are freely editable and are not proof of anything. Treat the output as a best-effort read, not identity.

## Privacy

Everything runs in your browser. The string you paste (or your own browser's User-Agent) never leaves your machine. Verify by viewing the page source or by opening DevTools and watching the network tab, no requests are made.

## Run locally

```bash
git clone https://github.com/0xelitesystem/user-agent-parser
cd user-agent-parser
# Open index.html in your browser, or:
python -m http.server 8000
```

## Build

There is no build. It's a single HTML file.

## License

MIT.

## Related

- [jwt-inspector](https://github.com/0xelitesystem/jwt-inspector), decode and verify JSON Web Tokens
- [curl-to-fetch](https://github.com/0xelitesystem/curl-to-fetch), convert curl commands to fetch and requests
- [webhook-signature-verifier](https://github.com/0xelitesystem/webhook-signature-verifier), verify webhook signatures

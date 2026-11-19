# Offline Global Persona Generator (`index.html`)

## Purpose
This web application makes synthetic global identities in a web browser for OSINT and OPSEC tasks. The application downloads the global dataset once into local IndexedDB storage. After the first load, the generator runs in browser memory with zero data transmission.

## GitHub Pages Deployment
1. Create a dedicated GitHub account over a VPN or Tor network.
2. Create a new repository.
3. Upload `index.html` to the root folder of the repository.
4. Open the repository **Settings**.
5. Select **Pages**.
6. Set the source branch to **main**.
7. Select **Save**.
8. Wait until GitHub publishes the site URL.

## First-Time Cache Setup
1. Connect your device to a VPN or Tor network.
2. Open the published GitHub Pages URL in a web browser.
3. Wait until the status badge shows `CACHED TO DISK` or `OFFLINE CACHE READY`.
4. Disconnect your device from the network to verify offline operation.

## Operation
1. Select a target country or `Random Global`.
2. Select a gender or `Random Gender`.
3. Select `Generate` to make a new identity.
4. Select `Copy Text`, `Copy CSV`, or `Copy JSON` to copy the output to the clipboard.

## Data Specifications
- **Coverage:** 34 identity fields across 16 countries.
- **National IDs:** Use unallocated prefixes (`666`, `900-999`, `ZZ`, or leading `0`). These numbers pass format checks only.
- **Email Addresses:** Use the `@example.com` domain (RFC 2606). These addresses do not receive mail.
- **Payment Cards and VINs:** Card numbers pass Luhn checks. Vehicle Identification Numbers pass ISO 3779 checks.

## OPSEC Rules and Limits
- **Public access:** GitHub Pages sites are public. Anyone with the URL can open the page.
- **Server logs:** GitHub servers log your IP address and browser metadata when you load `index.html`. Always connect through a VPN or Tor.
- **Account isolation:** Do not use your primary GitHub account or real Git email address in commits.
- **Storage isolation:** Browsers isolate IndexedDB storage by domain or local file path.
- **Private browsing mode:** Private windows delete IndexedDB storage when you close the browser. Use a standard browser profile to keep the offline cache.
- **Clipboard hygiene:** Delete copied identity data from your operating system clipboard history after use.

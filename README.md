# NOOR investor deck (QDB)

Web presentation for the NOOR pre-seed round. Live site: https://deck.noor.vip/ (password protected). GitHub Pages publishes the `main` branch automatically on every push; the `CNAME` file sets the custom domain, which Cloudflare DNS points at `noor-technologies.github.io`, and the old github.io address redirects there.

`index.html` is a small gate page. The deck and all of its images and clips are packed into one encrypted bundle (AES-256-GCM, key derived from the password with PBKDF2-SHA256) embedded in the page and decrypted in the browser once the password is entered, so nothing in this repository is readable without the password. The bundle is rebuilt from the deck source with a build script kept outside this repository.

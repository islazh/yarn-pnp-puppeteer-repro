This repo is a minimal reproduction of an issue with Yarn P'n'P and Puppeteer, specifically the postinstall step which downloads the browsers it needs to launch tests.

Steps to reproduce:
- `nvm use`
- `enable corepack`
- `yarn install`
- You should be able to see the error `Skipping browser installation because the Puppeteer build is not available. Run `npm install` again after you have re-built Puppeteer.`
- Chrome is NOT downloaded to `$HOME/.cache/puppeteer/chrome`

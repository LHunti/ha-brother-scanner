# Brother Scanner Add-on for Home Assistant (x86_64)

A simple, working Home Assistant add-on to use your USB-connected Brother scanner over the network. It uses the excellent **Scanservjs** web interface and includes the official **brscan4** Linux drivers.

## Why use this?
The original Scanservjs add-ons for Home Assistant are often outdated, failing with build errors (like the missing `run.sh` error) or broken download links. This version is specifically fixed for:
- **Architecture:** x86_64 (Intel NUC, Dell Optiplex, and other PC-based HA installations).
- **Driver:** Fixed `brscan4` download link directly from Brother.
- **Port:** Defaulted to `8124` to avoid common port conflicts.

## Installation
1. Go to your Home Assistant **Settings** -> **Add-ons** -> **Add-on Store**.
2. Click the three dots (⋮) in the top right and select **Repositories**.
3. Add the following URL: `https://github.com/LHunti/ha-brother-scanner`
4. Search for **Brother Scanner (Scanservjs)** and click **Install**.

## Configuration
- After installation, ensure your printer/scanner is **turned on** and connected via USB.
- In the add-on settings, go to the **Configuration** tab to change the network port if needed (default is `8124`).
- Start the add-on and open the **Web UI**.

## Supported Hardware
This add-on uses the `brscan4` driver. It's tested with the **Brother DCP-1510**, but should work with any Brother scanner supported by the `brscan4` package.

## Credits
- Based on [Scanservjs](https://github.com/sbs20/scanservjs).
- Inspired by the original (but broken) [ha-scanservjs-addon](https://github.com/niallr/ha-scanservjs-addon).

## License
MIT

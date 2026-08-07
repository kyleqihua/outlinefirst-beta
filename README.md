# watchbrief beta

watchbrief turns a supported YouTube video's captions into a concise, clickable
brief.

This repository is the public beta distribution channel. It contains the
installable extension package, release notes, checksum, privacy notice, and
product screenshot. The engineering source repository is currently private while
the product and licensing model are still being decided.

## Install

1. Open the
   [0.1.0 beta release](https://github.com/kyleqihua/watchbrief-beta/releases/tag/v0.1.0-beta.1).
2. Download `watchbrief.zip` and `watchbrief.zip.sha256`.
3. Unzip `watchbrief.zip`.
4. Open `chrome://extensions` in Chrome.
5. Turn on **Developer mode**.
6. Choose **Load unpacked** and select the unzipped `watchbrief` folder.
7. Open a supported YouTube video and choose **生成导读** in the watchbrief
   panel.

Chrome does not automatically update unpacked extensions. For a later beta,
replace the unzipped folder with the new release and choose **Reload** on the
extension card.

## Verify the download

On macOS:

```sh
shasum -a 256 -c watchbrief.zip.sha256
```

The command should print `watchbrief.zip: OK`.

## Privacy

When you choose **生成导读**, the video's captions and timestamps are sent
through the watchbrief Cloudflare Worker to DeepSeek. Do not use the beta for
private or confidential videos.

Read the complete [privacy notice](PRIVACY.md).

## Support

Open a GitHub issue with the video URL, Chrome version, and a screenshot of the
visible error. Do not include private captions, API keys, passwords, cookies, or
other credentials.

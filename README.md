# H-VNCareer developer website

Static GitHub Pages website for AnoBrowser, NijPath Browser, and Novalira. The root [`app-ads.txt`](app-ads.txt) contains the Google seller line found in `/home/jori/TT/app-ads.txt` at preparation time. **Confirm that `pub-2448331992138830` is the publisher ID shown in your AdMob account before publishing.** Add any other authorized seller lines supplied by the ad networks you actually use.

## Published URLs

- Developer website: https://hqa-tt.github.io/
- Ad seller file: https://hqa-tt.github.io/app-ads.txt

Both URLs returned HTTP 200 on 29 September 2026. GitHub Pages is configured to deploy from `main` and `/ (root)`.

## Connect the site to Google Play and AdMob

1. In the **Google Play Console listing contact details** for each app, enter `https://hqa-tt.github.io/` as the developer website. Enter the appropriate app-specific Privacy Policy URL separately:

   | App | Privacy Policy URL |
   | --- | --- |
   | AnoBrowser | `https://artemisx-sq01.github.io/legal/anobrowser/privacy.html` |
   | NijPath Browser | `https://artemisx-sq01.github.io/legal/nijpath/privacy.html` |
   | Novalira | `https://hqa-tt.github.io/legal/novalira/privacy.html` |

2. In AdMob, use **Apps → View all apps → app-ads.txt** to check the status. AdMob can take up to 24 hours to detect a changed Play listing or crawl the file. Its **Check for updates** action can request another crawl.

For future edits, commit locally and run `git push origin main`. The remote is `git@github-henry:HQA-TT/HQA-TT.github.io.git` on this machine.

The developer website must be a **site at the hostname root**, so a project Pages URL such as `https://hqa-tt.github.io/some-repo/app-ads.txt` is unsuitable as the primary location. A repository named `HQA-TT.github.io` publishes at the host root. Keep `app-ads.txt` in the top level of this repository.

GitHub Pages is the requested first host. Because `github.io` is a shared domain, confirm that **AdMob actually verifies each app**; successful browser access to the file alone is not proof of verification. If AdMob does not verify, point a domain you own to this same Pages site, put that domain in every Store listing, and check `https://your-domain/app-ads.txt`. No custom domain is configured yet.

References: [GitHub Pages setup](https://docs.github.com/en/pages/quickstart), [GitHub organization site naming](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site), [AdMob app-ads.txt setup](https://support.google.com/admob/answer/9363762?hl=en), [AdMob crawl checks](https://support.google.com/admob/answer/9679128?hl=en).

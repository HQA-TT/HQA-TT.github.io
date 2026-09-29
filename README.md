# H-VNCareer developer website

Static GitHub Pages website for AnoBrowser, NijPath Browser, and Novalira. The root [`app-ads.txt`](app-ads.txt) contains the Google seller line found in `/home/jori/TT/app-ads.txt` at preparation time. **Confirm that `pub-2448331992138830` is the publisher ID shown in your AdMob account before publishing.** Add any other authorized seller lines supplied by the ad networks you actually use.

## Publish to GitHub Pages

1. In the **HQA-TT** GitHub account, create a **public** repository named exactly `HQA-TT.github.io` (GitHub may normalize the URL to lowercase). Do not initialize it with a README; this local repository already has files.
2. From this directory, run:

   ```bash
   git remote add origin git@github-henry:HQA-TT/HQA-TT.github.io.git
   git push -u origin main
   ```

   If the SSH alias `github-henry` is unavailable on your machine, use the HTTPS remote shown by GitHub instead.
3. In the repository's **Settings → Pages**, set **Deploy from a branch → main → / (root)**, then Save. GitHub Pages should serve `https://hqa-tt.github.io/` and `https://hqa-tt.github.io/app-ads.txt`.
4. Open both URLs in a private browser window. The second URL must show the plain seller line, not an HTML page or 404.
5. In the **Google Play Console listing contact details** for each app, enter `https://hqa-tt.github.io/` as the developer website. Enter the appropriate app-specific Privacy Policy URL separately:

   | App | Privacy Policy URL |
   | --- | --- |
   | AnoBrowser | `https://artemisx-sq01.github.io/legal/anobrowser/privacy.html` |
   | NijPath Browser | `https://artemisx-sq01.github.io/legal/nijpath/privacy.html` |
   | Novalira | `https://hqa-tt.github.io/legal/novalira/privacy.html` |

6. In AdMob, use **Apps → View all apps → app-ads.txt** to check the status. AdMob can take up to 24 hours to detect a changed Play listing or crawl the file. Its **Check for updates** action can request another crawl.

The developer website must be a **site at the hostname root**, so a project Pages URL such as `https://hqa-tt.github.io/some-repo/app-ads.txt` is unsuitable as the primary location. A repository named `HQA-TT.github.io` publishes at the host root. Keep `app-ads.txt` in the top level of this repository.

GitHub Pages is the requested first host. Because `github.io` is a shared domain, confirm that **AdMob actually verifies each app**; successful browser access to the file alone is not proof of verification. If AdMob does not verify, point a domain you own to this same Pages site, put that domain in every Store listing, and check `https://your-domain/app-ads.txt`. No custom domain is configured yet.

References: [GitHub Pages setup](https://docs.github.com/en/pages/quickstart), [GitHub organization site naming](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site), [AdMob app-ads.txt setup](https://support.google.com/admob/answer/9363762?hl=en), [AdMob crawl checks](https://support.google.com/admob/answer/9679128?hl=en).

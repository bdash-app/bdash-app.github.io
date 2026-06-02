## Development

```
$ bundle install
$ bundle exec middleman server
```

## Deploy

This site is deployed by GitHub Actions to GitHub Pages.

Production URL: https://bdash-app.github.io/

1. Open the repository settings on GitHub.
2. Go to **Pages**.
3. Set **Source** to **GitHub Actions**.
4. Push to `master` or `main`, or run the `Deploy to GitHub Pages` workflow manually.

The workflow builds the Middleman site into `build/` and publishes that directory to GitHub Pages.

To use a custom domain, configure it in the GitHub Pages settings and add the required DNS records.

### Updating the download version

The site resolves the latest `bdash-app/bdash` release during the Middleman build. To update the version shown on the site after a Bdash release, trigger the `Deploy to GitHub Pages` workflow in this repository.

Recommended setup: add a release workflow in `bdash-app/bdash` that dispatches the `bdash-release` event to this repository when a release is published.

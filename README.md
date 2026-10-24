# PrivacyPolicy

Public product privacy policies. Only public policy content belongs in this repository.

- Policy index: https://changchiachi.github.io/PrivacyPolicy/
- Markdown Viewer Pro: https://changchiachi.github.io/PrivacyPolicy/ChromeExtension-Legal/

## Publishing

GitHub Pages uses **GitHub Actions** as its source. A normal push or pull request only checks and packages public files; it does not deploy. Production updates require a human to publish a **non-prerelease GitHub Release** with a `v`-prefixed tag, such as `v1.0.0`.

Draft releases, prereleases, ordinary commits, and tag pushes do not deploy. There is no manual workflow-dispatch deployment shortcut. The workflow deploys the release tag's exact commit, not whatever is currently at the tip of `main`.

The `github-pages` environment should allow deployment from tags matching `v*`. `.nojekyll` enables direct static HTML hosting. No application dependencies are required.

## Adding or updating a policy

1. Create `<Product>/index.html` with the policy in Chinese and English.
2. Describe actual data use, storage duration, deletion, third-party requests, and support contact details.
3. Update both language sections and their dates together when policy content changes.
4. Add the product link to `index.html` and this README.
5. Commit and push to `main`, then confirm the workflow's build job succeeds. Deployment should be skipped.
6. Open **Releases → Draft a new release**, create a new `v`-prefixed tag targeting the reviewed commit, and describe the policy changes. Do not select **Set as a pre-release**.
7. A human clicks **Publish release** when ready. Wait for the workflow's deployment job to succeed, then verify the public URL and the Chinese/English policy text.

When adding another product directory, also add it to the explicit copy list in `.github/workflows/pages.yml`. Only the selected public files are included in the site artifact.

To roll back, create a new release with a new tag pointing at the desired earlier commit that contains this workflow. Deleting a release does not restore an earlier website version.

Keep published product paths stable. If a page moves, retain a migration notice with the new link at its old location.

The Markdown Viewer Pro policy was migrated from `ChromeExtension-Legal` using the updated policy in `GitHubIO/docs/privacy/ChromeExtension/index.html`, including the per-tab reload cache disclosure. Its existing support Issues URL remains valid.

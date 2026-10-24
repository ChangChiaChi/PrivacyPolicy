# PrivacyPolicy

Public privacy policies for Thunder Studio products. Only public policy content belongs in this repository.

- Policy index: https://changchiachi.github.io/PrivacyPolicy/
- Markdown Viewer Pro: https://changchiachi.github.io/PrivacyPolicy/ChromeExtension-Legal/

## Publishing

GitHub Pages publishes the `main` branch's root directory. `.nojekyll` enables direct static HTML hosting. No build step or dependencies are required.

## Adding or updating a policy

1. Create `<Product>/index.html` with the policy in Chinese and English.
2. Describe actual data use, storage duration, deletion, third-party requests, and support contact details.
3. Update both language sections and their dates together when policy content changes.
4. Add the product link to `index.html` and this README.
5. Commit and push to `main`; verify the public URL after Pages finishes deploying.

Keep published product paths stable. If a page moves, retain a migration notice with the new link at its old location.

The Markdown Viewer Pro policy was migrated from `ChromeExtension-Legal` using the updated policy in `GitHubIO/docs/privacy/ChromeExtension/index.html`, including the per-tab reload cache disclosure. Its existing support Issues URL remains valid.

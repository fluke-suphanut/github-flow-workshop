# github-flow-workshop

A fork of a "Profile workshop for GitHubFlow" repository, where each attendee adds one HTML profile page through a pull request.

Portfolio: https://suphanut.pages.dev

## What it is

The exercise practises GitHub Flow:

1. Create a feature branch, for example `feature-<name>`.
2. Copy `profiles/template.html` to a new file in `profiles/` and edit it.
3. Commit, push the branch and open a pull request.
4. Merge the pull request into `main`.

The history has 57 merged pull requests. Most come from branches named `feature-<name>`.
The `profiles/` folder holds 55 profile pages and two template files.

## Files

| File | Purpose |
| --- | --- |
| `profiles/template.html` | Starting page with an image, a name heading and a short text, with Thai placeholder text. |
| `profiles/template copy.html` | A second, changed copy of the template. |
| `profiles/*.html` | One static profile page for each attendee. |
| `.vscode/settings.json` | Sets the VS Code Live Server port to 5501. |
| `.env` | Holds one comment line and no settings. |

## How to run

There is no build step. Open any file in `profiles/` in a browser, or use the VS Code Live Server extension.

To add a profile the same way as the attendees:

```bash
git switch -c feature-<name>
cp profiles/template.html profiles/<name>.html
# edit profiles/<name>.html
git add profiles/<name>.html
git commit -m "add <name> profile"
git push -u origin feature-<name>
```

Then open a pull request to `main` on GitHub.

## Example

`profiles/template.html` shows a 150-pixel image, an `<h1>` for the name and a `<p>` for a short introduction. Replace the Thai placeholder text with your own content.

## Limits

- This is a workshop exercise. There is no index page that links the profiles.
- The pages are static HTML. There are no tests or checks.
- Many profile images link to external sites, so some images may not load.
- The fork also has a remote feature branch with one more profile page. It is not merged into `main`.

## Licence

This repository is a fork. The content belongs to the original workshop repository and its contributors. The repository has no licence file, so default copyright applies.

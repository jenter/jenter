# jenter

> GitHub profile README repo (`jenter/jenter`): its README is shown on the GitHub profile page, and the only content is a pixel-art portrait image.

| | |
|---|---|
| Status | active |
| Stack | Markdown + one PNG image (no code) |
| Runs on | GitHub profile page (rendered by GitHub; nothing to deploy) |
| Last reviewed | 2026-11-26 |

## Architecture

- `README.md`: a single line, `<img src="./portrait-8bit.png">`, which GitHub renders on the profile page because the repo name matches the username.
- `portrait-8bit.png`: a 512×512 pixel-art ("8-bit" style) portrait, referenced by a relative path.
- There is no source code, build step, package manifest, CI workflow or config.
- The latest commit is "Delete me.gif", so an earlier `me.gif` image was removed in favour of the PNG.

## Reusable pieces

- `README.md`: shows how to embed a repo-local image on a GitHub profile README using a relative `<img>` path. Reuse it if you rebuild or restyle the profile page.
- `portrait-8bit.png`: a pixel-art avatar you could reuse as a profile picture or site favicon/avatar elsewhere.

## Integrations and credentials

None.

## Workflows

```sh
# Edit README.md or swap the image, then push to main; GitHub re-renders the profile automatically.
git add README.md portrait-8bit.png && git commit -m "Update profile" && git push
```

## Related repos

None identified from the repo contents.

## Gotchas

- The profile README only shows up because the repo name is the same as the GitHub username (`jenter/jenter`). Renaming the repo removes it from the profile.
- The image is linked by relative path (`./portrait-8bit.png`). If you rename or move the file, update the `<img>` tag too, or the profile shows a broken image.

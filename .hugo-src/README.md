# Rebuild the guides

This site uses Hugo 0.169.0 and PaperMod pinned by the theme submodule.
The published files are committed at the repository root so the existing
GitHub Pages branch deployment can serve them.

From the repository root, initialize the theme and build to a scratch directory.

```sh
git submodule update --init
build_dir=$(mktemp -d)
hugo --source .hugo-src --destination "$build_dir" --minify
cp -R "$build_dir"/. .
```

# ci.node

CI scripts for node deployments

```bash
mkdir -p .github/workflows/
curl https://raw.githubusercontent.com/signalwerk/ci.node/main/workflows/gh-pages.yml > .github/workflows/gh-pages.yml
```

## React projects

```sh
    "deploy": "npm run build && gh-pages --dotfiles -d build",
    .nojekyll
```

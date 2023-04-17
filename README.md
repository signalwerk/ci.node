# ci.node

CI scripts for node deployments

```bash
mkdir -p .github/workflows/
curl https://raw.githubusercontent.com/signalwerk/ci.node/main/workflows/gh-pages.yml > .github/workflows/gh-pages.yml
curl https://raw.githubusercontent.com/signalwerk/ci.node/main/workflows/ftp-deploy.yml > .github/workflows/ftp-deploy.yml
curl https://raw.githubusercontent.com/signalwerk/ci.node/main/workflows/update-readme.yml > .github/workflows/update-readme.yml
```

## React projects

```sh
    "deploy": "npm run build && gh-pages --dotfiles -d build",
    .nojekyll
```

## Used in project

- https://github.com/signalwerk/pixelfont.scanner
- https://github.com/signalwerk/webtypo
- https://github.com/signalwerk/sfgz
- https://github.com/signalwerk/signalwerk.styles

<!--
private projects
- https://github.com/signalwerk/lm-a/

-->

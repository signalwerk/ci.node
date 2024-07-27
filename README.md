# ci.node

## GH Pages Deployment

```bash
mkdir -p .github/workflows/
curl https://raw.githubusercontent.com/signalwerk/ci.node/main/workflows/gh-pages.yml > .github/workflows/gh-pages.yml
```

## FTP deployments

```bash
mkdir -p .github/workflows/
mkdir -p ci
curl https://raw.githubusercontent.com/signalwerk/ci.node/main/workflows/ftp-deploy.yml > .github/workflows/ftp-deploy.yml
curl https://raw.githubusercontent.com/signalwerk/ci.node/main/ci/lftp.sh > ci/lftp.sh
```

## Stamping files

```bash
mkdir -p ci
curl https://raw.githubusercontent.com/signalwerk/ci.node/main/ci/stamp.sh > ci/stamp.sh
```

```yaml
  - name: 🏷 stamp
    run: |
      bash ./ci/stamp.sh ./src/index.js
```


## Timebased deactivation of cronjobs

```bash
mkdir -p ci
curl https://raw.githubusercontent.com/signalwerk/ci.node/main/ci/deactivate.sh > ci/deactivate.sh
```

```yaml
  - name: 📅 Check date and deactivate cron if necessary
    run: |
      bash ./ci/deactivate.sh "2024-10-20" "gh-pages.yml"
    env:
      GH_TOKEN: ${{ github.token }}
```

## Configuring the default `GITHUB_TOKEN` permissions

[Adjust permission](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/enabling-features-for-your-repository/managing-github-actions-settings-for-a-repository#configuring-the-default-github_token-permissions)

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

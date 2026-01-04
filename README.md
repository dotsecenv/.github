# dotsecenv

[![CI](https://github.com/dotsecenv/dotsecenv/actions/workflows/ci.yml/badge.svg)](https://github.com/dotsecenv/dotsecenv/actions/workflows/ci.yml)
[![Release](https://github.com/dotsecenv/dotsecenv/actions/workflows/release.yml/badge.svg)](https://github.com/dotsecenv/dotsecenv/actions/workflows/release.yml)
[![GitHub Action E2E](https://github.com/dotsecenv/dotsecenv/actions/workflows/action-e2e.yml/badge.svg)](https://github.com/dotsecenv/dotsecenv/actions/workflows/action-e2e.yml)
[![Publish Packages](https://github.com/dotsecenv/packages/actions/workflows/publish.yml/badge.svg)](https://github.com/dotsecenv/packages/actions/workflows/publish.yml)
[![Homebrew install](https://github.com/dotsecenv/homebrew-tap/actions/workflows/post-release.yml/badge.svg)](https://github.com/dotsecenv/homebrew-tap/actions/workflows/post-release.yml)
[![Shell plugins CI](https://github.com/dotsecenv/plugin/actions/workflows/ci.yml/badge.svg)](https://github.com/dotsecenv/plugin/actions/workflows/ci.yml)
[![Publish Website](https://github.com/dotsecenv/website/actions/workflows/deploy-website.yml/badge.svg)](https://github.com/dotsecenv/website/actions/workflows/deploy-website.yml)

Manages encrypted secrets in your repositories, so you don't have to worry about accidentally leaking credentials!

### `dotsecenv` solves this problem:

```shell
echo "AWS_SECRET_ACCESS_KEY=your-secret-key" > .env
git add -A
git commit -m "..."
git push
# 😱 You've just leaked your credentials!
```

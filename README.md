# dotsecenv

Manages encrypted secrets in your repositories, so you don't have to worry about accidentally leaking credentials!

### Install

```bash
curl -fsSL https://get.dotsecenv.com/install.sh | bash
```

See [github.com/dotsecenv/dotsecenv](https://github.com/dotsecenv/dotsecenv#install-script-recommended) for all installation options.

### `dotsecenv` solves this problem:

```shell
echo "AWS_SECRET_ACCESS_KEY=your-secret-key" > .env
git add -A
git commit -m "..."
git push
# 😱 You've just leaked your credentials!
```

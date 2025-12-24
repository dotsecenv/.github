# dotsecenv

Manages encrypted secrets in your repositories, so you don't have to worry about accidentally leaking credentials!

### `dotsecenv` solves this problem:

```shell
echo "AWS_SECRET_ACCESS_KEY=your-secret-key" > .env
git add -A
git commit -m "..."
git push
# 😱 You've just leaked your credentials!
```

## Shell Plugins

Shell plugins that automatically load `.env` and `.secenv` files when entering directories
are available for `zsh`, `bash`, and `fish`.

```bash
curl -fsSL https://raw.githubusercontent.com/dotsecenv/plugin/main/install.sh | bash
```

For plugin manager installation and additional details, see [github.com/dotsecenv/plugin#installation](https://github.com/dotsecenv/plugin#installation).

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

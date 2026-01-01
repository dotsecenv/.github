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

## Installation

### Mise (universal)

```bash
mise use github:dotsecenv/dotsecenv
```

### MacOS/Homebrew

```bash
brew install dotsecenv
```

### Linux package managers

Package repositories for Debian/Ubuntu, RHEL/CentOS/Fedora, and Arch Linux are available at [get.dotsecenv.com](https://get.dotsecenv.com).

### Shell Plugins

Shell plugins that automatically load `.env` and `.secenv` files when entering directories
are available for `zsh`, `bash`, and `fish`.

For example, given a `/path/to/project/.secenv` file, e.g.:

```env
A_SECRET={dotsecenv}
ANOTHER_SECRET={dotsecenv/SOME_OTHER_KEY}
MY_NAMESPACED_SECRET={dotsecenv/my::SECRET}
```

The three keys will be available as environment variables, when cd-ing into `/path/to/project/`.

#### Install shell plugins

You can install zsh/bash/fish plugins with:

```bash
curl -fsSL https://raw.githubusercontent.com/dotsecenv/plugin/main/install.sh | bash
```

For plugin manager installation and additional details, see [github.com/dotsecenv/plugin#installation](https://github.com/dotsecenv/plugin#installation).

## How it works

`dotsecenv` uses GPG encryption to secure environment secrets within your repositories, eliminating the risk of plaintext leakages while maintaining the convenience of familiar `.env` files.

We aim to create a seamless security layer for your shell environment through:

- `dotsecenv` CLI: An intuitive command-line interface for managing encrypted secrets.
- **Shell Autocompletion**: Built-in autocompletion support for Bash, Zsh, and Fish
- `direnv`-like integration: conveniently decrypt and inject secrets directly into environment variables, on-demand.

## Core Features

- **GitOps friendly**: Stores secrets in encrypted _vault_ files that are safe to commit to version control systems.
- **GPG-based security**: Leverages standard GPG keys for encryption, decryption, and identity management.
- **Compliance**: FIPS 186-5 compliant algorithm defaults (RSA 2048+, ECC P-384+, EdDSA) with strict validation modes.
- **Collaboration**: Enables granular access control, allowing you to securely share secret material with users using their GPG public keys.

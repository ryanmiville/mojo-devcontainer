# Mojo Devcontainer

Rudimentary devcontainer template for the [Mojo programming language](https://docs.modular.com/mojo)

Dockerfile copied from the official [Mojo github repository](https://github.com/modularml/mojo/blob/19057520e9efe921fc15ad9daa9965d61d1ac5fd/examples/docker/Dockerfile.mojosdk)

## Instructions

VSCode will prompt you to open the dev container when you open the project. Do not do this yet. First you must add your Modular authentication key to `devcontainer.json`. To find your authentication key:

1. Log in at [developer.modular.com](https://developer.modular.com)
2. Copy your authentication key. You will find it in the install instructions that should look something like
```sh
curl https://get.modular.com | sh - && \
modular auth <YOUR_AUTH_KEY>
```
3. Set the `AUTH_KEY` environment variable in `devcontainer.json`
4. Once you save the file, vscode should prompt you to open the devcontainer again. Now you may do so.

The first build will take several minutes. Once it is complete, verify everything works by opening VSCode's integrated terminal and running `mojo hello.mojo`.

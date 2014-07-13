# Shell Completion

So you've build a fantastic node.js CLI, and even took the effort of adding `bash` or `zsh` completion files! However, now you're telling your users to add the sourcing of this file to their `.profile`, or similair intialization script..

No need! Simply add:

```shell
npm install shell-completion --save
```

And in your `package.json` use `shell-completion` to install the completion files:

```json
{ "scripts": {
  "postinstall": "install-completion bash myBashCompletion && install-completion zsh myZshCompletion"
} }
```


Shell-completion will link your completion files to the specified shell's and platform's default location.

## Features

* Supports Bash and Zsh
* Supports Homebrew installation prefixes on OS X
* Logs all errors if anything fails, but always exits without an error code. This means adding `install-completion` to your `postinstall` is completely safe, and will never break the rest of your application's installation!

## Usage

```
  Usage: link [options] [command]

  Commands:

    bash <completionfile>  Link <completionfile> for usage in bash
    zsh <completionfile>   Link <completionfile> for usage in zshell

  Options:

    -h, --help     output usage information
    -V, --version  output the version number
```

<p align="center"><a href="https://metacall.io/" target="_blank"><img src="https://github.com/metacall.png" width="28%"></a></p>

<h1 align="center"> <b> MetaCall Faas Deploy </b> </h1>

<p  align="center">Tool for deploying into MetaCall FaaS platform.</p>
<br>

[![NPM](https://img.shields.io/npm/v/@metacall/deploy?color=blue)](https://www.npmjs.com/package/@metacall/deploy)
[![Workflow](https://github.com/metacall/deploy/actions/workflows/ci.yml/badge.svg)](https://github.com/metacall/deploy/actions)
[![install size](https://packagephobia.com/badge?p=@metacall/deploy)](https://packagephobia.com/result?p=@metacall/deploy)
[![discord](https://img.shields.io/discord/781987805974757426?color=purple&style=plastic)](https://discord.com/channels/781987805974757426/)

## Table of Contents

-   [About](#about)
    -   [How to install](#how-to-install)
    -   [Configuration](#Configuration)
    -   [Token](#Token)
-   [Supported arguments and commands](#supported-arguments-and-commands)
-   [Exit codes and their meanings](#exit-codes-and-their-meanings)
-   [Contribute](#Contribute)
-   [License](#License)

## About

metacall-deploy provides the interface of options to deploy functions on Metacall FaaS platform. You can deploy your serverless functions within a few clicks without interacting with [Dashboard](https://dashboard.metacall.io/)

![giphyT](https://user-images.githubusercontent.com/65965202/209966480-5568a6da-5142-4259-a871-cc918e4855c1.gif)

## How to install

```bash
npm i -g @metacall/deploy
```

## Check installation

```bash
metacall-deploy --help
```

## Configuration

The configuration is stored in: - Unix: `$HOME/.metacall/deploy/config.ini` - Windows: `%APPDATA%\metacall\deploy\config.ini`

## Token

The token is stored in the configuration and can be overwritten at any time with `METACALL_API_KEY` environment variable.

## Supported arguments and commands

The metacall-deploy offers many commands for a variety of typical operations.

```bash
metacall-deploy --[args=value]
```

| CLI Args        | Description                                                                                                   |
| --------------- | ------------------------------------------------------------------------------------------------------------- |
| `--help`        | Prints a user manual to assist you in using the cli.                                                          |
| `--version`     | Prints current version of the cli.                                                                            |
| `--workdir`     | Accepts relative path to application directory, Defaults to `cwd`                                             |
| `--addrepo`     | Accepts url of repository to deploy                                                                           |
| `--projectName` | Accepts a string indicating the name of your project                                                          |
| `--email`       | Accepts email id for authentication                                                                           |
| `--password`    | Accepts password for authentication                                                                           |
| `--token`       | Accepts token for authentication, either pass email & password or token.                                      |
| `--force`       | Accepts boolean value: it deletes the deployment present on an existing plan and deploys again                |
| `--plan`        | Accepts type of plan: "Essential", "Standard", "Premium"                                                      |
| `--inspect`     | Accepts format of output : "Table", "Raw", "OpenAPIv3" and Lists out all the deployments with specifications. |
| `--delete`      | Accepts boolean value: it provides you all the available deployment options to delete                         |
| `--confDir`     | Accepts relative path for changing default config directory                                                   |
| `--logout`      | Accepts boolean value: use it in order to expire your current session.                                        |
| `--listPlans`   | Accepts boolean value: list all the plans that are offered in your account using it.                          |

## Ignore Files

If you don't want to deploy node modules or any other file, simply put it inside the .gitignore file as we use for ignoring files.

## Exit codes and their meanings

| Exit Code | Description          |
| --------- | -------------------- |
| `0`       | Success              |
| `1`       | NotDirectoryRootPath |
| `2`       | EmptyRootPath        |
| `3`       | NotFoundRootPath     |
| `4`       | AccountDisabled      |

## New to MetaCall? Create account and buy a plan

> Go to https://dashboard.metacall.io, signin and buy a plan. [Learn more...](https://metacall.io/doc.html#/faas/subs-plans)

## Contribute

> You Can Directly Start Contributing to this deployer in Cloud with ready to run, build & test the project.

[![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/#https://github.com/nshnt777/metacall-deploy)

To use it on your forked repo, edit the 'Open in Gitpod' button url to `https://gitpod.io/#https://github.com/<my-github-username>/deploy`

## License

This project is currently licensed under the [Apache License version 2.0](LICENSE).

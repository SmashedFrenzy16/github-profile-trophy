# Contribution Guide

## Environment

- Deno >= v1.36.1
- [Vercel](https://vercel.com/)
- GitHub API v4
- Docker and Docker compose (optional)

## Local Run

Create `.env` file to project root directory, and write your GitHub token to the
`.env` file. Please select the authority of `repo` when creating token.

```properties
GITHUB_TOKEN1=XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
GITHUB_TOKEN2=XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

# if using GitHub Enterprise:
# (this env var defaults to https://api.github.com/graphql)
GITHUB_API=https://github.example.com/api/graphql
```

Run local server.

```sh
deno task start
```

You can enable the Redis if you want, but it's not mandatory.

```sh
docker compose up -d
```

Rename `env-example` to `.env`, and change ENABLE_REDIS to true

Open localhost from your browser.

http://localhost:8080/?username=ryo-ma

## Editor config

Read the [.editorconfig](./.editorconfig)

## Run deno lint

If you want to contribute to my project, you should check the lint with the
following command.

```sh
deno lint --unstable
```

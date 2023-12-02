# Go (Golang) Codespaces starter template

docker in docker を使用して、codespaces 環境の中で、Docker 環境を作成し go を動かせるようにしました。

## Hello World

1. codespaces を作成する
   右上の`Use this template`>`Create a new repository`をクリックして、リポジトリを作成する。

2. リポジトリを作成出来たら、右上の`Code`から`Codespaces`タブをクリックして、 `Create codespace on main`をクリックする。

3. codespaces のターミナルで以下のコマンドを実行する

```bash
cd app
go run hello.go
```

## Dockerfile を利用したい場合

1. 任意の Dockerfile を、`/.devcontainer`直下に作成します。
2. `/.devcontainer/devcontainer.json`を編集します。

```
  // ~~~ 省略 ~~~

  // imageの指定
  // "image": "mcr.microsoft.com/devcontainers/go:0-1.20-bullseye",
  // 任意のDockerfileを利用する場合は、以下のコメントアウトを外し同じ階層にDockerfileを配置して、imageをコメントアウト。
  "build": {
    "dockerfile": "Dockerfile"
  },

  // ~~~ 省略 ~~~
```

## refs

- https://github.com/devcontainers
- https://containers.dev/guide/dockerfile#docker-compose

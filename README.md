### Inspired by https://github.com/ohbarye/rails-react-typescript-docker-example

## TL;DR

**Here is an example application with the following modern web technology stacks. With this boilerplate, you can easily start to build your own app.**

- [Ruby](https://www.ruby-lang.org/en/) 2.7.2
- [Rails](https://rubyonrails.org/) (API mode) 6.1.0
- [Nuxt.js](https://nuxtjs.org/) 2.8.1
- [TypeScript](https://www.typescriptlang.org/) 3.5.1
- [Docker](https://docs.docker.com/)
- [PostgreSQL](https://www.postgresql.org/)

## Usage

### `.env`

```
POSTGRES_USERNAME=postgres
POSTGRES_PASSWORD=xxxxxx
```

### Run localhost

```shell
$ git clone https://github.com/samuraikun/rails-nuxt-typescript-docker-example.git && cd rails-nuxt-typescript-docker-example

# Setup
$ docker-compose build

// Gemfileを変更した場合
$ docker-compose run web bundle install
$ cd frontend && yarn install
$ docker-compose run backend bin/rails db:create

# Start
$ docker-compose up -d

$ // Rails
$ open http://localhost:8000
$ // Nuxt
$ cd frontend && yarn run dev
$ open http://localhost:4000
```

#### Gemfileを変更した場合 or docker-compose up後、gemが見つからないというエラーの場合
- `docker-compose run web bundle install` を実行
    - https://qiita.com/hokita222/items/49f4ca54835e08fdd6b2

## Motivation

Nowadays, I feel like **we need a wide range acknowledgment on web development even if we call ourselves "backend developer" or "frontend developer".**


The SPA, Of course, has a backend API, Ruby on Rails connecting PostgreSQL in my case. I use Docker Compose for defining and running multi-container Docker applications because it's not much simple to bootstrap all of applications and middlewares.

**Learning each technology itself is not a burden. I rather like learning. But I've thought I'd like to pursue my playground whose tech stacks are virtually same as ones I develop in work.**


## Further Details

### Backend

The combination, Rails + PostgreSQL + Docker Compose, is just a result I followed [Docker Compose's official instruction](https://docs.docker.com/compose/rails/).

### Frontend

Bootstrapped with [create-nuxt-app](https://github.com/nuxt/create-nuxt-app).

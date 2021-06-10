# Overview

#### Features

- Automatically generate a self-documenting **GraphQL** /  **REST API** from an existing database.

- Maintain API endpoints and validation rules with a **single config file**.

- Deploy & serve any **static site generator**.

- Built with [Express](https://expressjs.com), [Apollo](https://www.apollographql.com), [Prisma](https://www.prisma.io), and [TypeScript](https://www.typescriptlang.org/).


#### Installation

##### 1. Clone the repo

```
git clone https://github.com/platform-kit/platformkit-api api
```

##### 2. Install dependencies

```
cd api
npm install
```

##### 3. Add the config

Since the main function is to generate an API form a database, you will need to provisoin and configure a database. The database must not be empty (otherwise there would be no need for an API).

If you're starting from scratch (an empty database), you can get started quickly by adding a [Prisma schema](https://www.prisma.io/docs/concepts/components/prisma-schema) at `/app/prisma/schema.prisma`.

Alternatively, if you've already got a repository with a `/prisma/` directory (including at least a `prisma.schema` file), specify the `GITHUB_REPOSITORY` and `GITHUB_TOKEN` environment variables in your `.env` file. Then run `npm run pull` to clone the repo.
# TypeGraphQL-Prisma with Apollo server

This project is to explore the possibility of `typegraphql-prisma`, a tool to generate GraphQL resolver from Prisma schema.

This project is mainly follow the instructions from [this article](https://dev.to/prisma/prototyping-a-crud-api-with-typegraphql-and-prisma-for-your-database-424c).

## Instruction

1. `cp .env.example .env` and fill in PostgreSQL url to `DATABASE_URL` in `.env`
2. `npm i`
3. `npm run prisma:push` if database table is not yet created
4. `npm run dev` and browse `http://localhost:4000/`

## Queries

- find many and find first query: filter, sort, cursor, pagination
- find one query (what is the difference between `user` and `getUser` ?)
- aggregation query: avg, count, max, min, sum
- group by query: mixture of find many and aggregation, just like group by in SQL

## Mutations

- create many and create one
- update many and update one
- delete many and delete one
- upsert many and upsert one

## Features

- [Authorization](https://prisma.typegraphql.com/docs/advanced/additional-decorators) in [TypeGraphQL way](https://typegraphql.com/docs/0.16.0/authorization.html)
- Exposing selected [models](https://prisma.typegraphql.com/docs/advanced/exposing-models) or [actions](https://prisma.typegraphql.com/docs/advanced/exposing-actions)
- DateTime type supported by default
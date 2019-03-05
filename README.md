# Prisma Connection

Repo to show issue generating schema from datamodel.

See original problem [here](https://github.com/prisma/prisma/issues/3629#issuecomment-468024433).

## Prerequisites

1. `npm install -g prisma@1.27.4`

## Steps to reproduce

1. See `datamodel.prisma` has `posts: [Post!]!` relationship on `User` type
2. `prisma generate`
3. See generated `User` model does not have a `postsConnection` as would be expected. There is only a `PostsConnection` on the root `Query` type.

At this point, if you created the schema using the postgresql adapter, your `schema.prisma` should look like this:

```javascript
generator client {
	provider = "prisma-client-js"
}

datasource db {
	provider = "postgresql"
	url      = env("DATABASE_URL")
}
```

To define new schemas we can define it as such. 
```javascript
model User {
    id       Int      @id @default(autoincrement())
    name     String
}
```

We have now defined a User model, but we haven't updated the database. To add this model to the database we need to run the following command in the terminal:
```bash
npx prisma migrate dev --name init
```

`migrate` pushes a migration 
`dev` refers to the development environment 
`--name init` sets the name to 'init'

After running the command, it is recommended to restart the typescript server in your code editor. 



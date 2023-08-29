You can only ever have one datasource. Prisma directly connects to the database. 
```javascript
datasource db {
	provider = "postgresql"
	url      = "env('DATABASE_URL')"
}
```
It is important to store connection strings in an environment variable. 

It is important to use a client generator specific to the platform/library you're developing on. 
```javascript
generator client {
	provider = "prisma-client-js"
}
```
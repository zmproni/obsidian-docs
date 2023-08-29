Based on my understanding almost all client methods are asyncronous, this is important to keep in mind. 

Lets say we want to create a new user, we can do so like this:
```javascript
const user = await prisma.user.create({
	data: {name: "kyle"}
});
```

This code will send a request to the database to create a new user, then return the user back to the caller. We will store the new user in the variable and print it out with:
```javascript
console.log(user)
```

The program so far will look like this:
`script.ts`
```javascript
import { PrismaClient } from '@prisma/client'
const prisma = new PrismaClient()

async function main() {
    const user = 
	    await prisma.user.create({data: {name:"Kyle"}});
}

main()
    .catch(e => {console.error(e)})
    .finally(async () => {await prisma.$disconnect()})
```

If we modify `package.json`'s script:
```json
...
"scripts": {
	"dev": "nodemon script.ts"
}
...
```

When we run:
```bash
npm run dev
```

We will get the output for the `script.ts` file. 

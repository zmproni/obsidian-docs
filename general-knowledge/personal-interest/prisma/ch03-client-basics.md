We have created a new prisma client code that now contains methods to inrract with the database models defined. 
```
✔ Generated Prisma Client (4.16.1 | library) to .\node_modules\@prisma\client in 43ms
```

We need to install the prisma client library to interract with the client.
```
npm i @prisma/client
```

If you need to manually regenerate your client, you can run the following command:
```bash
npx prisma generate
```

If you want to begin using the code, in your index or server file you can add the following lines of code:
```javascript
import { PrismaClient } from '@prisma/client'
const prisma = new PrismaClient()
```

Thanks to using typescript, when you type:
```javascript
prisma.
```
You will get code autocompletion for various methods and properties, including 'user' as the client code now contains methods defined based on the schema previously provided. 
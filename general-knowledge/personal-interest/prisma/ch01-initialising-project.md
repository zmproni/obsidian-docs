This command imports required dependencies and the optional typescript and its type definitions for node.js.
`terminal`
```bash
npm i --save-dev prisma typescript ts-node @types
```

`tsconfig.json`
```json 
{
    "compilerOptions": {
        "sourceMap": true,
        "outDir": "dist",
        "strict": true,
        "lib": ["ESNext"],
        "esModuleInterop": true
    }
}
```

`terminal`
```bash
npx prisma init --datasource-provider <provider>
```
This generates a basic prisma file in a folder called prisma in the root directory. The file will contain basic default values  for based on the provider passed. 

The list of available providers can be found at: **TO BE FOUND**

The list of generated files include:
`root/`
	`.env`
	`prisma/
		`schema.prisma`

The `.env` file expects the database URL for prisma to connect to. The database management system must be running and the database must exist. 


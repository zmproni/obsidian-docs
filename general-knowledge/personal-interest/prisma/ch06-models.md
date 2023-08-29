Each model represents a table in your database. Each model is composed of fields and each field is composed of 4 different parts. 

```
model User {
	id    Int      @id @default(autoincrement())
	name  String   
	email String?
}
```

This can be summarised as:
```
model ModelName {
	fieldName     Type[field type modifier] @attributes ...
}
```
This [link](https://www.prisma.io/docs/reference/api-reference/prisma-schema-reference#attributes) contains a list of attributes.

A list of data types supported on prisma
```
model DataTypes {
	string        String
	int           Int
	bigInt        BigInt
	boolean       Boolean
	float         Float
	decimal       Decimal
	dateTime      DateTime
	blob          Bytes
	json          Json 
	relationship  <ModelName>       // Eg: author User
	unsupported   Unsupported("")
}
```




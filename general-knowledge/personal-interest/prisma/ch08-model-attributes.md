
**Field Level Attributes**
Defined to the right of the field data type
|Attribute| Description |
|---|---|
|`@default`|Allows the definition of default values|
|`@id`|Defines the field as the id of the table|
|`@unique`|A constraint that says the field value must be unique|
|`@relation`|Define table relationships|
|`@updatedAt`|Whenever the row is updated, the value will be set to the current timestamp|
|`@default(now())`|Time row was created|

**Block Level Attribute**
Defined at the bottom of a model definition. 
```
model User {
	//id    String     @id @default(uuid())
	name  String  
	email String
	
	@@unique([name, email])   // Name+Email needs to be unique
	@@index([email])          // Create an index on the field
	@@id([name, email])       // Composite ids
}
```



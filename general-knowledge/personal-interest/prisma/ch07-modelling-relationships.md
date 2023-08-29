There are various numbers of relationships that can be modelled within prisma:
* One to one
* One to many
* Many to many

### One to Many 
**A user can have many posts.**
```
model User {
	id    String     @id @default(uuid())
	name  String  
	Post  Post[]
	
}

model Post {
	id        String  @id @default(uuid())
	rating    Float
	author    User    @relation(fields: [authorId], references: [id])
	authorId  String
}
```

**Disambiguating Multiple One to Many Relationships**
```
model User {
	id       String     @id @default(uuid())
	name     String  
	written  Post[]     @relation('writtenPosts')
	starred  Post[]     @relation('starredPosts')
}

model Post {
	id        String  @id @default(uuid())
	rating    Float
	authorId  String
	starredId String?
	
	author    User    @relation('writtenPosts', fields: [authorId], references: [written])
	
	starredBy User?   @relation('starredPosts', fields: [starredId], references: [starred])
}
```


### Many to Many 
```
model Category {
	id        String   @id @default(uuid())
	posts     Post[]   
}

model Post {
	id          String  @id @default(uuid())
	categories  Category[]
}
```

### One to One
```
model User {
	id              String            @id @default(uuid())
	name            String  
	userPreference  UserPreference?    
}

model UserPreference {
	id            String    @id @default(uuid())
	emailUpdates  Boolean   
	userId        String    @unique 
	user          User      @relation(fields:[userId], references[id])
}
```
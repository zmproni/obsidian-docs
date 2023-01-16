Markdown to Medium article typewriter. 
1. Reads Markdown file
2. Opens up Medium.com
3. Creates a new article
4. Starts typing it down 
5. Publishes it 

Could be written in:
- Python 3
- Rust ??? 
- Java

Idea for interface:
1. A shell script written in Rust
You run the command specifying the file, name of the article etc... and it just runs. 

2. A Python 3 package that provides an API to perform various actions
Create a Python package that allows other people to use the API to create their own typewriter bots. Also has the feature to parse and type on Medium a whole Markdown document. 

Difficulties:
Parser would have to be able to handle writing code blocks, format the page. 

Required Knowledge
- String manipulation 
- Document parsing techniques 
- Web drivers
- Selenium 
- Time 
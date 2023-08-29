```javascript
const selected = canvas.tokens.controlled; selected.forEach(element => { let value = (element.document.displayName === 50)? 20 : 50; element.document.displayName = value; element.document.update({displayName: value}); element.refresh(); });
```

# Good Regular Expression to Validate username

```
/^(?=.{8,20}$)(?![_.])(?!.*[_.]{2})[a-zA-Z0-9._]+(?<![_.])$/
```

`(?=.{8,20}$)` - username is 8-20 characters long

`(?![_.])` - no _ or . at the beginning

`(?!.*[_.]{2})` - no __ or _. or ._ or .. inside

`[a-zA-Z0-9._]` - allowed characters

`+(?<![_.])` - no _ or . at the end

## More simple version

```
^(?=.*$)(?![_])[a-zA-Z0-9_]+(?<![_])$
```

**Allows:** 
1. username of any length
2. numbers and _

**Doesn't allow:**
1. start or end with _


---
[Link to Stackoverflow](https://stackoverflow.com/questions/12018245/regular-expression-to-validate-username)

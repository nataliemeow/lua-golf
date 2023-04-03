# Lua golfing manual

This manual is a work-in-progress guide for code-golfing in Lua.

## Practices to shorten

These practices usually make code shorter. Do these if applicable, and of course, only if shorter.

### Minimize whitespace

This should go without saying, but minimize whitespace (spaces, tabs, newlines). More in [Omit whitespace](#omit-whitespace).
```lua
-- instead of:
while true do
	if (...) then
		(...)
	else
		(...)
	end
end
-- do this:
while true do if (...) then (...) else (...) end end
-- or even this:
while''do if (...) then (...) else (...) end end

### Use global variables

```lua
-- instead of:
local x=1
-- do this:
x=1
```

### Rename functions

Rename functions to one-letter variables.
```lua
-- instead of:
print('this')print('that')print('those')
-- do this:
p=print p('this')p('that')p('those')
```

### Omit whitespace

Many tokens don't need whitespaces after them to seperate them from others. Here is a list;
- `(`, `)`
- `{`, `}`
- `[`, `]`
- `'`, `"`
- `...`
...and there are these ones, but you probably know them already; `#`, `%`, `&`, `*`, `+`, `,`, `-`, `.`, `..`, `/`, `//`, `:`, `<`, `<=`, `=`, `==`, `>`, `>=`, `^`, `|`, `~`, `~=`.
```lua
-- instead of:
if y then print('yes')else print('no')end
--                   ^^              ^^
--       Notice how there's no whitespace.
```

### Use the ternary operator
Use an `and`/`or` ternary operator instead of an `if` statement.
```lua
-- instead of:
if x then a=y else z end
-- do this:

```

## Shorter ways to do common tasks

### Infinite loop

```lua
while''do
while""do
while{}do (...) end
```

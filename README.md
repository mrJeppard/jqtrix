# jqtrix
A reference for common tasks with jq, the bash json parser. 

Snippets: One liners 
Sugar scripts: Examples of how to make scripts with jq command.

## Scripts
First arg for all scripts is 'key', 2nd is optional file path.

bin/del: delete all matching keys anywhere in the json

## Snippets
```
# delete all keys matching 'leaf'
cat simple.json | jq 'del(.. | .leaf?)'
```



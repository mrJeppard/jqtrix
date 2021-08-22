# jqtrix
A reference for common tasks with jq.

## Scripts
First arg for all scripts is 'key', 2nd is optional file path.

bin/del: delete all matching keys anywhere in the json

## Snippets
```
# delete all keys matching 'leaf'
cat simple.json | jq 'del(.. | .leaf?)'
```
```
# function to add key value
add(){
    KEY=$1
    VALUE=$2
    jq --arg KEY $KEY --arg VALUE $VALUE 'map(.[$KEY] = $VALUE)'
}
cat simple.json | add new key
```




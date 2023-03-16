# vscode regex stuff

## Laravel
### Add return type to eloquent relationships
Find
```regex
(function [a-zA-Z]+\(\))([\s\r\n]+\{[\s\r\n]+return \$this->(has(?:(?:One|Many)(?:Through)?)|belongsTo(?:Many)?|Morph(?:To|One|Many))\((?:(?:[a-zA-Z]+)::class|__FUNCTION__))
```
Replace
```regex
$1: \u$3$2
```

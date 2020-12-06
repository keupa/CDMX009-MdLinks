![mdlinks-title](readme-img/title.png)
*keupa-mdlinks* is a library for node.js that allows the user to extract links from a markdown file (.md) and verify the status ( 200 or 404 ).

## Install

```
$ npm i keupa-mdlinks
```

## CLI Usage
```
$ keupa-mdlinks --file <path-to-file>
```
## Options
##### `--validate // --v`
The module makes an http request, validates the link, and returns the HTTP status. 
Example: 

```
$ keupa-mdlinks --validate --file <path-to-file>
Validated links from your ./test/links.md file: 
   ⋆ href: https://www.google.com/idhucda status: 404 FAILED✕
   ⋆ href: http://superbad.com/1/turkey/viv.html status: 200 OK✓
   ⋆ href: http://lewisatkins.com/projects status: 200 OK✓
```

##### `--stats // --s`
The module returns the links basic stats.
Example:
```
$ keupa-mdlinks --stats --file <path-to-file>
Your file ./test/links.md contains: 
   ⋆ Total: 3
   ⋆ Unique: 3
```
##### `--stats --validate // --s --v`
The module makes an HTTP requests and returns validated stats.
Example:

```
$ keupa-mdlinks --stats --validate --file <path-to-file>
Your file ./test/links.md contains: 
   ⋆ Total: 3
   ⋆ Unique: 3
```

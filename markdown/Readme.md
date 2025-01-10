## Markdown Example

- [unordered lists](#unordered-lists)
- ordered lists
- text formatting
- code
- tables
- blockquotes
- autolists
- lists
- images
- [links](#links)

https://github.github.com/gfm/

## Unordered lists

We can create unordered lists using hyphen

+ foo
+ bar
- baz

## Ordered lists

1. foo
2. bar
<!-- # Same number will just increament automatically -->
3) baz 
3) baz
3) baz

## Text formatting

*italics*
**bold**
__bold__
~~strikethrough~~

## Code

### Inline code

You can print to the terminal using the `puts "hollow world"` command

### Multi line code

#### Without highlighting

```
def hello_world
    puts "Hello world"
end
```

#### With highlighting

```rb
def hello_world
    puts "Hello world"
end
```

### Tables

| foo | bar |
| --- | --- |
| baz | bim |

| abc | defghi |
:-: | -----------:
bar | baz

 <!-- If there are a number of cells fewer than the number of cells in the header row, empty cells are inserted. If there are greater, the excess is ignored -->
| abc | def |
| --- | --- |
| bar |
| bar | baz | boo |


## Blockquote

   > # Foo
   > bar
 > baz

 > # Foo
> bar
> baz


## Links

[Github Website](https://githb.com)

[Secret Page](./secret.md)



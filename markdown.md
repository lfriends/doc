**Remember**:
- You should put blank lines before and after a heading for compatibility. eg: #_heading_  (_ stands for spacing)
- To create paragraphs, use a blank line
- Don't put tabs or spaces in front of your paragraphs.

# Table of contents

* [Headings](heading-level-1-)
* [Line Breaks](line-breaks)
* [Horizontal Rule](horizontal-rule)
* [Emphasis](emphasis)
* [Sorted Lists](sorted-lists-1)
* [Unsorted Lists](unsorted-lists)
* [Qutes](quotes)
    *[Code quote](code-quote)
    *[Block quote](block-quote)
    *[Fenced code block](fenced-code-block)
    *[Lines quotes](lines-quote)
* [Links & Images](links--images)
* [Emoji](emoji)
* [Table](table)
* [Task List](task-list)
* [External references](external-references)




# Heading level 1 `#`
## Heading level 2 `##`
### Heading level 3 `###`
#### Heading level 4 `#####`
##### Heading level 5 `#####`
###### Heading level 6 `######`

Heading level 1 (alterntate )  `===============` <br>
Heading level 2 (alterntate )  `---------------`

## Line Breaks

To create a line break or new line (`<br>`), end a line with **two or more spaces**, and then type return.

You can use two or more spaces (commonly referred to as “trailing whitespace”) for line breaks in nearly
every Markdown application, but it’s controversial. It’s hard to see trailing whitespace.<br>
For this reason itis better to use the `<br>` tag.

## Horizontal Rule
\---

## Emphasis
- **Bold** :arrow_right: `**`
- *Italic* :arrow_right: `*`
- ***Bold & Italic*** :arrow_right: `***`
- ~srikeout~ :arrow_right: `~srikeout~`
- color <font color="red">red!</font> :arrow_right: use HTML :arrow_right: `<font color="red">red!</font>`

NOTE: also `__`__Undercores__`__` does the trik in pace of `**`**stars**`**`. But with Underscores you have always to put a blank space before and after!<br>
eg: `(space)__`__Undercores__`__(space)`




## Sorted Lists `1.`
Remember: the number you type does not effect the order.

eg:  
    \ 5. First item  
    \ 5. Second items  
    \ 0. Third items  
becomes:  

5. First item  
5. Second items  
0. Third items

## Unsorted Lists `-`
To create an unordered list, add dashes (-), asterisks (*), or plus signs (+) in front of the Items.  
But remeber: not to mix them!
- item
- item
    - Indented item (2tabs)

**Unordered List Items With Numbers**

you can use a backslash (\) to escape the period.
- 1988\. Escape from New York  
`- 1988\. Escape from New York`


## Quotes 

##### Code quote  

\`code\`  
This is a `code`.

##### Block quote  


to block a quote, add 1 tab or 4 spaces

\_ _ _ _\<html> ...

    <html>
      <head>
      </head>
    </html>
    
##### Fenced code block 


\```  ... \```
```
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```
##### Lines quotes

\> ...  

> Line 1 
> > Line2 





## Links & Images

Link \[title\](https://www.example.com)

Image \!\[alt text\](image.jpg)

**IMAGE SIZE**  
Markdown syntax doesn’t allow you to specify image size.  
But supports HTML TAGS

`<img src="image.png" width="200" height="100">`








## EMOJI

*  [emoji shotrcodes](https://gist.github.com/rxaviers/7360908)  `:joy:` :joy: `:tent:` :tent: `:smile:` :smile: `:poop:` :poop: `:yum:` :yum: [...]
     

*  [emoji images](https://emojipedia.org/large-red-square/) 🚀


## Table 

```| Item| Price| # In stock |
|-----|-----|---------|
| Juicy Apples | 1.99| *7*|
| Bananas| **1.89**  | 5234|
```


| Item| Price| # In stock |
|-----|-----|---------|
| Juicy Apples | 1.99| *7*|
| Bananas| **1.89**  | 5234|


## Task List 	
- [x] Write the press release
- [ ] Update the website
- [ ] Contact the media 


## External references

* [basic-syntax](https://www.markdownguide.org/basic-syntax)
* [GitHub Markdown documentation](https://docs.github.com/en/get-started/writing-on-github)
* [emoji shotrcodes](https://gist.github.com/rxaviers/7360908)
* [emoji images](https://emojipedia.org/large-red-square/)
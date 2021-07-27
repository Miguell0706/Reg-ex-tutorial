# RegEx- Matching an E-mail



## Summary

 In this homework, I will be breaking down the regex used to 
 validate if an piece of text fits the criteria to be an email-adress.
 The following is the regex expression. 
 ```
 Matching an Email: /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
 ```
## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [Character Escapes](#character-escapes)
- [Author](#author)

## Regex Components
```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```
## Anchors
Anchors in this regex include the carrot('^') and dollar sign ('$')
```
^ $
```
The carrot in regex is used to specify that a text must begin with a specified criteria, in this case the user inputting the e-mail must input a line of text where the beginning of the text is either any letter between a-z or number between 0-9 or an underscore, period, or dash('_','.','-')

The dollar sign in regex is used to specify that a text must end with a specified criteria, in this case the user must end their input with a text that ends with any characters between a-z or a period('.') and these sequence of characters must have a length of at least 2-6.

## Quantifiers
Quantifiers in regex are used to specify a minimum, maximum, or range of length in a text. The quantifiers are expressed in regex with a curly bracket '{}' and can have a range of options to specify length. In this regex they are using a number and a larger number seperated by a comma to inidicate that the text must have between 2 - 6 characters or instances of matched patterns.
```
{2,6}
```
The plus sign indicates that the text must match the pattern at least one or more times. In this regex it would force the user to create a text that would be at least one character followed by an @ and another text of at least one character in length. 
```
+
```
## Grouping Constructs
Grouping Constructs allow for the seperation of sections in a regex expression. In this regex epxression there are a few isntances of grouping construts. The first would be. . .
```
([a-z0-9_\.-]+)
```
This expression means that it is looking for any characters between a-z 0-9 and it would also accept a period, underscore or dash, and this text must be at least one character in length. The second grouping construct is seperated from this one by a literal (meaning it must match the exact criteria) '@'.
```
([\da-z\.-]+)
```
This expression is looking for any number between 0-9 (\d), or as any character between a-z, or a literal period or dash. This text must also be at least one character in length.

```
([a-z\.]{2,6})
```
This grouping construct is at the end of the expression and will looking for a ".net, .gmail, .yahoo ,etc..." to be in the end of the text. It is doing this by looking for any character between a-z or a literal period and this text must be between 2-6 characters in length.
## Bracket Expressions
Bracket expressions ```[]```
in regex are used to specify a set of single or multiple character elements. In this regex expression brackets are used mainly for finding if the text contains a character of a-z or any number between 0-9 and literal underscores, periods and dashed are also used in the bracket expression of this regex.

## Character Classes
Character classes defines a set of characters. Bracket expressions count as a character class which this regex utilizes. Other common character classes are the aforementioned ```\d``` which looks for any digit between 0-9 or ```\w``` which looks for any alphanumeric character as well as the underscore. This regex utilizes the ```\d``` in this piece of the regex expression ```([\da-z\.-]+)```

## Character Escapes

Character escapes in this regex are used to specify the literal text instead of using its' special properties. This is done by putting a back slash ``` \ ``` before the text.
in this expression the backwards slash is seen before the period in some of the bracket expression. This is done because the period ``` . ``` without the backwards slash would signify a wildcard character meaning any character in its place would be a valid for the regex to accept. With the backwards slash this ``` . ``` loses that special property and becomes a literal ``` . ``` which will be useful for the email formatting. 

## Author

If you have any questions, you can contact me at Miguellozano3757@gmail.com.

If you would like to see my profile, my github is [Miguell0706](https://github.com/Miguell0706)


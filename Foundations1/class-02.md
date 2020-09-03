# Class-02 Reading Notes
### HTML & CSS
#### Chapt. 2 'Text'
* When adding webpages you add tags (known as markup) tags help later
* Structural Markup: the elements that you can use to describe both heading and paragraphs
* Semantic Markup: which provides extra info. Example such as where emphasis is placed in a sentence.
* Heading ```<h1>``` through ```<h6>``` six levels h1 used for main heading and h2 is used for sub heading. If a subheading is needed within a subheading use h3 and so on
* ```<p>``` to create a paragraph. Each new paragraph it is put in a new line.
* Enclosing words in either ```<b></b>``` or ```<i></i>``` give you (b = bold) and (i = italic)
* ```<sup>``` gives you superscript and ```<sub>``` gives you subscript
* whitespace to make things easier to read
* ```<br />``` line break and ```<hr />``` horizontal rules create a break between themes
* ```<strong>``` indicates that the content has strong importance. Everything in the element will be bold.
* ```<em>``` add emphasis will be in italic
* Quotations ```<blockquote>``` and ```<q>```
* ```<abbr>``` is an abbreviation. A title attribute on the opening tag is used to specify the full term
* ```<cite>``` for citations
* ```<dfn>``` for definitions
* ```<address>``` contains contact details for the author of the page. element in italics
* ```<ins>``` element can be used to show content that has been inserted into a document while ```<del>``` element can show text that has been deleted from it.

### Chapt. 10 'Introducing CSS'
* Imagine an invisable box around every HTML element
* Block and inline elements
* CSS allows you to create rules that control the way that each individual box and the contents of the box is presented.
* Selectors indicate which element the rule applies applies to. The same rule can apply to more than one element if you seperate the elements names with commas
* Declarations indicate how the element reffred to  in the selector should be styled. Declarations are split into two parts property followed by value
* Properties indicate the aspects of the element you want to change.
* Values specify the setting you want for the property
* When using an external CSS file you must ```<link>``` it to the html file 
* For in html styling you can use ```<style>```
* css selectors must keep in mind. 
* Cascading Styles must make sure css is placed corectly to avoid problems with cascading

### JavaScript
#### Chap. 2 'Basic JS Instuctions'

* Each individual instruction or step is known as a statement. Should end with a ;
* {} indicate start and end of code block
* comments //
* variables let and const
* set variable to something with =
* use quotes to indicate a string
* can only change the value of let variables
* an array store multiple values within it. can be done using brackets []
strings, number, and booleans

#### Chap. 4 'Decisions & Loops'
* Flowchart to help plan decision making. 
* Two components to a decision 1. an expression is evaluated which returns a vallue (true/false) 2. a conditional statement syays what to do in a given situation (if/then/else)
* == equals to
* === strict equals to 
* != is not equal to
* !=== strict not equal to
* && test more than one condition
* || this operator test at least one condition
* ! this operator takes a single boolean value and inverts it
* if statement evaluates or checks a condition. if the condition evaluates to true any statements in subsequent code block are executed
*  if...else statements checks a condition. if it resolves true the first code block is executed if the condition resolves false the second code block is executed


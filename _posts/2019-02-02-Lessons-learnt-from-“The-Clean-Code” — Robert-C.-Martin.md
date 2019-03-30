
<img src="https://systemscue.it/wp-content/uploads/2018/11/1-nWkAm-cuh_XSUdH-rSic8g-1.jpeg"
width="1000" height="400"/>

I recently read my Clean Code, the famous book by the prolific Uncle bob martin and it was one of the eye opening experiences of my life as a programmer. This book has given me a lot of knowledge on what are the best practises and how to actually write code. Now I feel ashamed of my coding skills. Though I always strive to better my code, this book has taught a lot more.

Now, you are reading this blog for two reasons. First, you are a programmer. Second, you want to be a better programmer. Good. We need better programmers.

## What is Clean Code, anyway?
Imagine being in a record store, and you are looking for some albums. If the store sorted and categorized their albums, you will find your albums faster. In addition, the cool interior design & architecture will make the whole experience much comfortable. Clean code is like that well organised, sophisticated record store.

<p>    There are two types of programming. Good programming and bad programming. Even bad code works. But it is not enough for code to work. It should be understandable at once, readable and scalable. It should not make other developers scratch their head in frustation! So how do we achieve it? The following way :</p>

## Characteristics of a Clean code
* Elegant: Clean code is pleasing to read, should make you smile.
* Readable: Clean code should read like well-written prose.
* Simple: Do one thing with the Single Responsibility Principle (SRP).
* Testable: Run all the tests.

## Meaningful Names
>“You should name a variable using the same care with which you name a first-born child.” 
>“There are only two hard things in Computer Science: cache invalidation and naming things” — Phil Karlton
<p>   Everything in an application has a name, from variables, functions, arguments, classes, modules, to packages, source file, directories.

Naming things is the most common problem of every developer. A good name will make understanding the code much easier. Uncle Bob has shared some simple rules to create good names:
### Do's:
<b>Use intention-revealing Names</b>
<p>The name should tell you why it exists, what it does, and how it is used. If a name requires a comment, it is a bad name. 
var a = 0 # the name a reveals nothing : bad .
var age = 0; # : good
</p>

<b>Use Pronounceable Names</b>
<p>Humans are good at words and words are, by definition, pronounceable.
If you can’t pronounce it, you can’t discuss it without sounding like an idiot. This matters because programming is a social activity.
  edvbn = circle.radius # : bad
  circle_radius = circle.radius # : good
 </p>
 
<b>Class Names</b>
<p>Classes and objects should have noun or noun phrase names like Customer, WikiPage, Account, and AddressParser. Avoid words like Manager, Processor, Data, or Info in the name of a class.
A class name should not be a verb.</p>

<b>Method Names</b>
<p>Methods should have a verb or verb phrase names. Examples: createUser, deletePhoto or save</p>

<b>Pick One Word per Concept</b>
<p>One and the same concept in your application should have the same name. For example, it’s confusing to have fetch, retrieve, and get as equivalent methods of different classes.
Using the same word per concept will help developers more easy to understand the code.</p>

### Don'ts:
<b> Encodings </b>
<p>Encoded names are seldom pronounceable and are easy to mistype.</p>

<b> Mental Mapping </b>
<p>Readers shouldn’t have to mentally translate your names into other names they already know. This problem generally arises from a choice to use neither problem domain terms nor solution domain terms. 
One difference between a smart programmer and a professional programmer is that the professional understands that clarity is king. Professionals use their powers for good and write code that others can understand.</p>

<b> Pun </b>
<p>Avoid using the same word for two purposes. Using the same term for two different ideas is essentially a pun.</p>

## Functions
A Function should do one thing only and do it really well
### Certain tips for writing effective functions:

* Avoid passing boolean into a function, this is a hint that func has an if statement within which causes it to do more than one thing.
* Functions should either do something or answer something, but not both. This ensures a function does not have hidden side effects. e.g a func named isEven() should only return a bool and not do any other operations
* Prefer Exceptions to Returning Error Codes and extract error handling try catch into their own function.
* Avoid output arguments. Function if it has to, should change state of its owning object
* Code should always be separated with blank line to club logical blocks together. Think of different lines of code as thoughts and then always think of organizing similar thoughts together
* Each function should read like a newspaper, every functions implementation following its call and having less vertical density
* Don’t return null

## Comments
<p>If you are writing comments to prove your point, you are doing a blunder. Ideally, comments are not required at all. If your code needs commenting, you are doing something wrong. Our code should explain everything. Modern programming languages are english like through which we can easily explain our point. Correct naming can prevent comments.</p>

## Unit Tests
 > “Code, without tests, is not clean. No matter how elegant it is, no matter how readable and accessible, if it hath not tests, it be unclean. Dave” ― Robert C. Martin
<p>The Test Driven Development (TDD): It is a software development process that relies on the repetition of a very short development cycle: requirements are turned into very specific test cases, then the software is improved to pass the new tests, only.</p>

Uncle Bob describes TDD with 3 laws:

* First Law: You may not write production code until you have written a failing unit test.
* Second Law: You may not write more of a unit test than is sufficient to fail, and not compiling is failing.
* Third Law: You may not write more production code than is sufficient to pass the currently failing test.

So folks, that's it. This surely does not include all the details of clean code but it can help you get basics of clean code right. We also have many tools available to help writing clean code. I will be introducing them in my upcoming blog-posts.
Till then, happy clean-coding!











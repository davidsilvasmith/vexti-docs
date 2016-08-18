# Writing HTML

We prefer to use slim for writing HTML.

It takes the noise out of the HTML spec which reduces errors, bugs, and increases productivity.

That being said there is a learning curve.

Here are the things to know.

1. Slim is whitespace sensitive. Use two spaces for indentations, not tabs.
2. The most common issue I run into is doing this:
div Some content
  ul
   li First item
Slim will render that like: Some content ul li first item.
The issue is 'Some content' after the div. Fix it like this:
div
  span Some content
    ul
      li First item
3. Running code. In slim use a `-` to signify a line of code like this:
- first_name = 'dave'
The equivalent ERB code would be:
<% first_name = 'dave' %> (see the noise?)
4. String replacement - use #{variable} to input strings, like this:
div Name: #{@contact.name}
or like this:
a href="mailto:#{contact.email}" #{contact.name} (will result in <a href="mailto:contact@email.com">dave</a>)
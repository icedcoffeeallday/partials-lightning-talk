##I'm partial to partials ... And so can you!

###What's cool about them?
 - Reduce loads of code to a single line!
 - Rails lets you use the _same_ form for edit and create functions, including the button. No more rendering erb with a separate button!
 - Reduce clutter in long HTML files: using a partial for headers and footers keeps your page code short and sweet, and DRYs your page code right up!

###When can I use them?
 - Headers!
 - Forms forms forms!
 - Error messages!
 - Responses!
 - Rendering collections OMG!

###What's different with Rails?
 - No need to use a long line like `erb :'/_form, layout: false, locals {post:@post}`
 - Instead, use `<%= render '_form'`. That was super easy, right?
 - But ... How do I pass variables now that locals is MIA? See below ...

###Making your partials
 - You know the basics on this one!
 - Don't forget your CSS tags — but be careful with the `id` tag if this partial is going to be used repeatedly.
 - Passing variables
     - Calling your partial: `<%= render '_form', title: "Best Title EVER"`
     - In the partial, this plays out like: `<title><%= title %></title>`

###Organizing your partials
 - _Layout_-specific partials go in `app/views/layouts`
 - _Controller_-specific partials go in `app/views/<controller_name>`
 - _Application_ partials go in `app/views/application`

###Rendering Collections ... Wait, what? No more .each?
 - Rails offers a relationship between a partial called `_article.html.erb` and a plural-named instance variable `@articles` called as an argument in `<%=render @articles%>`. It'll then display whatever you coded in the partial (a nice unordered list, a table, p tags, whatevs) for each article. No more giant .each statement.



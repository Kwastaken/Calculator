# Breakdown of code changes

## HTML

1. No structural changes

### ID's vs Classes vs Data-

I changed where you stored what value each button had from an ID to a data- attribute. It works and I don't think that putting it as an ID was wrong but it can lead to some misunderstandings by other developers. For example I ended up breaking the delete button style for a little while because I did not realize that you used the i.d both for the value of the button and to style it. My rule of thumb I would give you is to use Id's solely for referencing an element. If you need to store some data with an element do that with a data-foo attribute, like in this case the number or operator was data. I was able to use the data attribute in the javascript to determine whether it was a number or an operator.

### Calling functions in HTML

It's a personal preference but I really do not like calling javascript functions in vanilla HTML. In this case however, it would save you a lot of work by adding an event listener to a group of elements like I did.

## CSS

1. I only made one change in CSS, if you find yourself re-writting styles for similar elements, add a selector that can style them at the same time. I created a selector that selected all the text fields at the same time to give them the same background and remove their border.

## Javascript

**Use less variables and functions**

- You had a total of 14 variables, and 7 functions. I was able to achieve the functionality with 9 variables and 4 functions. It comes with practice but always remember, you probably need less variables than you think and you should only create them when necessary. Some things that you think you need a variable to store are logically implied.

For example:

1. You made a variable to check if the an operator was clicked. I simply used an if-statement
2. You made a variable to check if the operator clicked was the equal sign. I simply gave the data-type as operator, and added the equal sign to the switch statement responsible for checking what operator was clicked.
3. In the case of the '.' it could simply be added to the number so there was no need for a variable for that.
4. Numbers have no logic to them, all you needed to do was add it to the number currently there. With that in mind I reduced the function you created to handle number input from 13 lines to 1

It will come with more practice bro :thumbsup:

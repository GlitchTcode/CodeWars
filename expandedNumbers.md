# My Awesome Project

You will be given a number and you will need to return it as a string in Expanded Form. For example:<br>

expandedForm(12); // Should return '10 + 2'<br>
expandedForm(42); // Should return '40 + 2'<br>
expandedForm(70304); // Should return '70000 + 300 + 4'<br>

NOTE: All numbers will be whole numbers greater than 0.<br>

How It's Made:

Tech used: JavaScript

Starting off I knew I had to turn the Number into a string so I could manipulate the number as an array and can test each digit. I test each digit against num > 0 to make sure it's above zero and then add it to my new expanded array multiplied by ten to the power of the length of the array minus 1 and the index of the current element of the array. My initial attempt had me using .map but my utilization was having problems during testing so I switched to using .forEach in order to iterate through the array and store the value in expand.
Optimizations




**Link to project:**
Here was my final answer:<br>
function expandedForm(num) {<br>
  let arr = num.toString().split('')<br>
  let expand = []<br>
  arr.forEach((x, ind) => {<br>
    if (x > 0) {<br>
      expand.push(x * (10**((arr.length - 1) - ind )))<br>
    }<br>
  })<br>
  return expand.join(' + ')<br>
}<br>

![alt tag](http://placecorgi.com/1200/650)


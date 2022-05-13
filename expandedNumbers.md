
function expandedForm(num) {<br>
let arr = num.toString().split('')<br>
  &emsp;let expand = []<br>
  &emsp;&emsp;arr.forEach((x, ind) => {<br>
    &emsp;&emsp;&emsp;if (x > 0) {<br>
      &emsp;&emsp;&emsp;&emsp;expand.push(x * (10**((arr.length - 1) - ind )))<br>
    &emsp;&emsp;}<br>
  &emsp;})<br>
  &emsp;return expand.join(' + ')<br>
}<br>

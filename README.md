# Jaden-Case


## Problem
Jaden Smith, the son of Will Smith, is the star of films such as The Karate Kid (2010) and After Earth (2013). Jaden is also known for some of his philosophy that he delivers via Twitter. When writing on Twitter, he is known for almost always capitalizing every word. For simplicity, you'll have to capitalize each word, check out how contractions are expected to be in the example below.

Your task is to convert strings to how they would be written by Jaden Smith. The strings are actual quotes from Jaden Smith, but they are not capitalized in the same way he originally typed them.

Example:

Not Jaden-Cased: "How can mirrors be real if our eyes aren't real"
Jaden-Cased:     "How Can Mirrors Be Real If Our Eyes Aren't Real"


## Solution 1
```javascript
String.prototype.toJadenCase = function () {
//   assign 'this' keyword to a variable and split string into an array
  var result = this.split(" ");
  
//   loop through the array changing first character of each item uppercase & adding it to the remaing letters in each item
  for(let i = 0; i < result.length; i++) {
   result[i] = result[i].charAt(0).toUpperCase() + result[i].substring(1);
  }
//   return items joined back together in a string
  return result.join(' ');
}
}

var str = 'hello darling'
str.toJadenCase('hello darling');

```

## Solution 2  
```javascript
String.prototype.toJadenCase = function () {

  function capitalizeFirstLetter(string) {
      return string.charAt(0).toUpperCase() + string.slice(1);
  }
  
  return this.split(' ').map(capitalizeFirstLetter).join(' ');
};
var str = 'hello darling'
str.toJadenCase('hello darling');
```

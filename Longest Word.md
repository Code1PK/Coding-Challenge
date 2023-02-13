# [Longest Word](https://www.coderbyte.com/editor/Longest%20Word:JavaScript)

### Understanding the problem

Have the function `LongestWord(sen)` take the `sen` parameter being passed and return the longest word in the string. If there are two or more words that are the same length, return the first word from the string with that length. Ignore punctuation and assume `sen` will not be empty. Words may also contain numbers, for example "Hello world123 567" 

<pre>
<b>Input:"fun&!! time"
<b>Output:</b> time
<b>Input:</b> "I love dogs"
<b>Output:</b> love
</pre>

#
### Approach: Built-In Functions

### Implementation
```js
function LongestWord(sen) { 
  let sepSen = sen.split(' ');
  let longWord = "";
  for(let i=0; i<sepSen.length; i++){
    if(sepSen[i].length > longWord.length){
      longWord = sepSen[i];
    }
  }
  return longWord; 
}
   
console.log(LongestWord("fun&!! time"));
```

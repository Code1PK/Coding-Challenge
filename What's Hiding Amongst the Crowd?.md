# What's Hiding Amongst the Crowd?

### Understanding the problem

A word is on the loose and now has tried to hide amongst a crowd of tall letters! Help write a function to detect what the word is, knowing the following `rules:`

- The wanted word is in lowercase.
- The crowd of letters is all in uppercase.
- Note that the word will be spread out amongst the random letters, but their letters remain in the same order.

<pre>
<b>Input:</b> detectWord("UcUNFYGaFYFYGtNUH")
<b>Output:</b> "cat"
<b>Input:</b> detectWord("bEEFGBuFBRrHgUHlNFYaYr")
<b>Output:</b> "burglar"
</pre>

#
### Approach: For Loop 

### Implementation
```js
function detectWord(string){
  let lowercase = "";
  for(let i=0; i<string.length; i++){
    if (string[i] === string[i].toLowerCase()){
      lowercase += string[i];
    }
  }
  return lowercase;
};
```

# [Older Than Me](https://edabit.com/challenge/iwdZiFucR5wkQsFHu)

### Understanding the problem

Create a method in the `Person` class which returns how another person's age compares. Given the instances `p1`, `p2` and `p3`, which will be initialised with the attributes `name` and `age`, return a sentence in the following format:

`{other person name} is {older than / younger than / the same age as} me.`

<pre>
<b>Input:</b> 
p1 = Person("Samuel", 24)
p2 = Person("Joel", 36)
p3 = Person("Lily", 24)
<b>Output:</b>
p1.compareAge(p2) ➞ "Joel is older than me."
p2.compareAge(p1) ➞ "Samuel is younger than me."
p1.compareAge(p3) ➞ "Lily is the same age as me."
</pre>

#
### Approach: Conditions

### Implementation
```js
class Person{
  constructor(name, age){
    this.name = name;
    this.age = age;
  }

compareAge (b){
  if(b.age > this.age){
    return `${b.name} is older than me.`
  } else if(b.age < this.age){
    return `${b.name} is younger than me.`
  } else {
    return `${b.name} is the same age as me.`
  }
}

p1 = new Person("Samuel", 24);
p2 = new Person("Joel", 36);
p3 = new Person("Lily", 24);

console.log(p1.compareAge(p2)); 
  // ➞ "Joel is older than me."

console.log(p2.compareAge(p1)); 
  // ➞ "Samuel is younger than me."

console.log(p1.compareAge(p3));
  // ➞ "Lily is the same age as me."
```

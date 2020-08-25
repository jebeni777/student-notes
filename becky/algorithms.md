### Code Wars
### Get the mean of an array 

It's the academic year's end, fateful moment of your school report. The averages must be calculated. All the students come to you and entreat you to calculate their average for them. Easy ! You just need to write a script.  

Return the average of the given array rounded down to its nearest integer.  

The array will never be empty.  


```
function getAverage(marks){
  let sum = 0;
  for (let i = 0; i< marks.length; i++) {
    sum += marks[i];
  }
  return Math.floor(sum / marks.length);
} 
```


### Code Wars
### Smallest unused ID

You've got much data to manage and of course you use zero-based and non-negative ID's to make each data item unique!  

Therefore you need a method, which returns the smallest unused ID for your next new data item...  

Note: The given array of used IDs may be unsorted. For test reasons there may be duplicate IDs, but you don't have to find or remove them!  

``` 
function nextId(ids){
  const arr = new Set(ids);
    for (let i = 0; i <= ids.length; i++) {
      if (!arr.has(i)) {
        return i;
      }
    }
}
```


### Code Wars
### Keep Hydrated!

Nathan loves cycling.  

Because Nathan knows it is important to stay hydrated, he drinks 0.5 litres of water per hour of cycling.  

You get given the time in hours and you need to return the number of litres Nathan will drink, rounded to the smallest value.  

For example:  

time = 3 ----> litres = 1  

time = 6.7---> litres = 3  

time = 11.8--> litres = 5  

```
function litres(time) {
  return Math.floor(time * 0.5);
}
```


### Code Wars
### Simple directions reversal

In this Kata, you will be given directions and your task will be to find your way back.  

```
solve(["Begin on Road A","Right on Road B","Right on Road C","Left on Road D"]) = ['Begin on Road D', 'Right on Road C', 'Left on Road B', 'Left on Road A']
solve(['Begin on Lua Pkwy', 'Right on Sixth Alley', 'Right on 1st Cr']) =  ['Begin on 1st Cr', 'Left on Sixth Alley', 'Left on Lua Pkwy']
```

### my solution
```
function solve(arr){
  let res = []; 
  let a = [];
  for (let i of arr) 
    a.push(i.split(' '));
  res.push('Begin ' + a.slice(-1).pop().slice(1).join(' '));
  for (let i = a.length-1; i > 0; i--) {
    a[i][0] === 'Right' ? res.push('Left ' + a[i-1].slice(1).join(' ')) : 
      res.push('Right ' + a[i-1].slice(1).join(' '));
  } 
  return res;
}
```

### Code Wars
### Multiplication table

Your task, is to create NxN multiplication table, of size provided in parameter.  

for example, when given size is 3:  
```
1 2 3
2 4 6
3 6 9
```
for given example, the return value should be: [[1,2,3],[2,4,6],[3,6,9]]  

### my solution
```
multiplicationTable = function(size) {
  var arr = []
  for (var i = 1; i <= size; i++ ) {
    var result = [];
    for (var j = 1; j <= size; j++) {
      result.push(j*i);
    }
    arr.push(result);
  }
 return arr;
}
```



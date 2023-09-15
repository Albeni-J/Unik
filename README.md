
```
let input1 = prompt();
let input2 = prompt();

let arr1 = input1.split(" ");
let arr2 = input2.split(" ");

let common = []; //undefined

for(let i = 0; i < arr1.length; i++){
    for(let j = 0; j < arr2.length; j++){
        if(arr1[i] === arr2[j]){
            if(!common.includes(arr1[i])){
                common.push(arr1[i]);
            }
        }
    }
}

alert(common);

```

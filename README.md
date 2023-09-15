\\1 Даны два массива: А[M] и B[N] (M и N вводятся с клавиатуры).
Необходимо создать третий массив минимально возможного
размера, в котором нужно собрать общие элементы двух массивов
без повторений.
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

///2 Даны два массива: А[M] и B[N] (M и N вводятся с клавиатуры).
Необходимо создать третий массив минимально возможного
размера, в котором нужно собрать элементы массива A, которые не
включаются в массив B, без повторений.

let input1 = prompt();
let input2 = prompt();

let a1 = input1.split(" ");
let a2 = input2.split(" ");

let common = [];

for (let i = 0; i < a1.length; i++) {
  for (let j = 0; j < a2.length; j++) {
    if (a1[i] === a2[j]) {
        if (!common.includes(a1[i])){
            common.push(a1[i]);
        }
    }
  }
}

let ans = [];   

for( let i = 0; i < a1.length; i++) {
    if (!common.includes(a1[i]) ) {
        if (!ans.includes(a1[i])) {
            ans.push(a1[i]);
        }
    }
}

for( let i = 0; i < a2.length; i++) {
    if (!common.includes(a2[i]) && !ans.includes(a2[i])) {
        ans.push(a2[i]);
    }
}

alert(ans);



/// 4 Создать функцию, позволяющую добавлять блок элементов в конец
массива.

let array = [1 , 2 , 3];
let block = [7, 2 ,4 ];




// array =  add(array,block);



function add(array, block) {
    for(let i = 0; i < block.length; i++){
        array.push(block[i]);
    }
    
}
add(array, block)
    


 console.log(array);

/// 5 Создать функцию, позволяющую вставлять блок элементов,
начиная с произвольного индекса массива.
let array = [1 , 2 , 3];
let block = [7, 2 ,4 ];
let index = 1;
// 1 2 7 2 4 3
// 1 2 [7 2 4] 3
let answer = [];

function add(array, block, index){
    let arr = [];

    for (let i = 0; i <= index; i++){
        arr.push(array[i]);
    }

    arr.push(...block);
    
    for (let i = index+1; i < array.length; i++){
        arr.push(array[i]);
    }

    return arr;
}

alert(add(array, block, index));


/// 5 Даны два массива: А[M] и B[N] (M и N вводятся с клавиатуры).
Необходимо создать третий массив минимально возможного
размера, в котором нужно собрать элементы массивов A и B,
которые не являются общими для них, без повторений.



let input1 = prompt();
let input2 = prompt();

let a1 = input1.split(" ");
let a2 = input2.split(" ");

let common = [];

for (let i = 0; i < a1.length; i++) {
  for (let j = 0; j < a2.length; j++) {
    if (a1[i] === a2[j]) {
        if (!common.includes(a1[i])){
            common.push(a1[i]);
        }
    }
  }
}

let ans = [];   // a1 = 1 1 2 3 4
                // common = 2 3
                // answer = 1

for( let i = 0; i < a1.length; i++) {
    if (!common.includes(a1[i]) ) {
        if (!ans.includes(a1[i])) {
            ans.push(a1[i]);
        }
    }
}

alert(ans);

"# Week-3-Assignment" 
/*<script src = "Week3Assign.js"></script>*/

//1. DONE Create an array called ages that contains the following values: 3, 9, 23, 64, 2, 8, 28, 93.
var agesArray = [3, 9, 23, 64, 2, 8, 28, 93];

//a. DONE Programmatically subtract the value of the first element in the array from the value in the last element of the array (do not use numbers to reference the last element, find it programmatically, ages[7] – ages[0] is not allowed). Print the result to the console.

let firstNumber = agesArray[0];
console.log(firstNumber);

let lastNumber = agesArray[agesArray.length - 1];
console.log(lastNumber);

function differenceLastFromFirst(lastNumber, firstNumber){
    let difference = (agesArray[agesArray.length - 1]- agesArray[0]); 
       console.log(difference);
}

differenceLastFromFirst(); //gives me -90

//b. DONE Add a new age to your array and repeat the step above to ensure it is dynamic (works for arrays of different lengths).
agesArray.push(17);
console.log(agesArray);

console.log(agesArray[agesArray.length - 1]);
differenceLastFromFirst();

//c.DONEUse a loop to iterate through the array and calculate the average age. Print the result to the console.
let sumAgeArray = agesArray.reduce(function(accumulator, currentValue){
    return accumulator + currentValue;
});
console.log(sumAgeArray);
console.log(sumAgeArray / agesArray.length);

//2.DONE Create an array called names that contains the following values: ‘Sam’, ‘Tommy’, ‘Tim’, ‘Sally’, ‘Buck’, ‘Bob’.

var namesArray1 = ['Sam', 'Tommy', 'Tim', 'Sally', 'Buck', 'Bob'];
console.log(namesArray1);

//a.Use a loop to iterate through the array 

let nameLengths1 = namesArray1.map(function(name){
    return name.length;
});

console.log(nameLengths1);

//DONE and calculate the average number of letters per name. Print the result to the console.
let nameLengths1Sum = nameLengths1.reduce(function(accumulator, currentValue){
    return accumulator + currentValue; 
});
console.log(nameLengths1Sum); //Sum of all name lengths
console.log(nameLengths1Sum / namesArray1.length); //average of name lengths


//b.DONE Use a loop to iterate through the array again and concatenate all the names together, separated by spaces, and print the result to the console.

const namesArray3 = namesArray1.concat(nameLengths1);
console.log(namesArray3);


//3. DONEHow do you access the last element of any array?
console.log(namesArray1[namesArray1.length - 1]);

//4.DONE How do you access the first element of any array?
console.log(namesArray1[0]);

//5. DONE Create a new array called nameLengths. Write a loop to iterate over the previously created names array and add the length of each name to the nameLengths array.

var namesArray2 = ['Kelly', 'Sam', 'Kate'];
console.log(namesArray2);

let nameLengths2 = namesArray2.map(function(name){
    return name.length;
});

console.log(nameLengths2);


//6. DONE Write a loop to iterate over the nameLengths array and calculate the sum of all the elements in the array. Print the result to the console.

nameLengths2Sum = nameLengths2.reduce(function(accumulator, currentValue){
    return accumulator + currentValue; 
});

console.log(nameLengths2Sum); //Sum of all name lengths
console.log(nameLengths2Sum / namesArray2.length); //average of name lengths

//7.	Write a function that takes two parameters, word and n, as arguments and returns the word concatenated to itself n number of times. (i.e. if I pass in ‘Hello’ and 3, I would expect the function to return ‘HelloHelloHello’).

function repeatedWord(word, n){
    if (i = 0, i < n, i++){ //<-- this is the error....how do i get it to repeat?
        return(word);
    }
}

console.log(repeatedWord("Hello",3));

//8.DONE	Write a function that takes two parameters, firstName and lastName, and returns a full name (the full name should be the first and the last name separated by a space).

let firstName = ["Rebekah", "Joshua", "Ericka"]; 
let lastName = ["Mann", "Dauner", "Clark"];

function fullName(firstName, lastName){
  return (firstName + " " + lastName);
};

console.log(fullName(firstName[1], lastName[1]));
console.log(fullName("Rebekah", "Mann"));

//9.DONE	Write a function that takes an array of numbers and returns true if the sum of all the numbers in the array is greater than 100.
//reduce & filter --> Doesn't quite work as a function when values are changed.

let numbers = [5, 17, 24, 6, 8, 1, 30, 28, 7, 10];
let numbers2 = [1,8,2,19,2,22,6,22,10,11,9,23,5,3,9,5];


numbersSum = numbers.reduce(function(accumulator, currentValue){
    return accumulator + currentValue; 
});
console.log(numbersSum);

function greaterThan100(){
    if(numbersSum > 100){;
        console.log(true);
    }else console.log(false);
}

greaterThan100();

//10.	Write a function that takes an array of numbers and returns the average of all the elements in the array.
//reduce
// i can't figure out how to do a function with an average. his will take more time later!
let array1=[6,17,30];
let array2 = [8,1,28];

let array1Sum = array1.reduce(function(accumulator, currentValue){
    return accumulator + currentValue; 
});
console.log(array1Sum);



function arrayAverage(array1Sum,length){
    let array1average = (array1Sum / array1.length) ; 
    console.log(array1average);
}

console.log(arrayAverage());

//11.DONE	Write a function that takes two arrays of numbers and returns true if the average of the elements in the first array is greater than the average of the elements in the second array.
//reduce & filter

let array2Sum = array2.reduce(function(accumulator, currentValue){
    return accumulator + currentValue; 
});
console.log(array2Sum);

let array2average = (array2Sum / array2.length) ;
console.log(array2average);


function arrayAverageComparison(array1Average, array2Average){
    if(array1average > array2average){
        console.log(true);
    }else{
        console.log(false);
    }
};

//arrayAverageComparison(array1average, array2average);

//12. DONE Write a function called willBuyDrink that takes a boolean isHotOutside, and a number moneyInPocket, and returns true if it is hot outside and if moneyInPocket is greater than 10.50.
let isHotOutside = true;

function willBuyDrink(isHotOutside, moneyInPocket){
    if(isHotOutside == true && moneyInPocket > 10.50){
        console.log(true);
    }else {
        console.log(false);
    }
} 

willBuyDrink(isHotOutside, 10.51);
willBuyDrink(isHotOutside, 10.49);

//13.Create a function of your own that solves a problem. In comments, write what the function does and why you created it

let isSunday = true;

function willGoGolfing(isSunday, bankBalance){
    if(isSunday == true && bankBalance >54.05){
        console.log("We get to golf!");
    }else {
        console.log("Budget better next month.");
    }
}

willGoGolfing(isSunday, 35.92); //this should return false b/c not enough money
willGoGolfing(isSunday, 55); //this should return true 
isSunday = false; 

willGoGolfing(isSunday, 55); //this should return false b/c not Sunday
willGoGolfing(isSunday, 45); //this should return false b/c not enough money && not Sunday

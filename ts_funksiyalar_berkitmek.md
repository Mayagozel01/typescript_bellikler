### 1 exercise.
#### // Write a function called "twoFer" that accepts a person's name
#### // It should return a string in the format "one for <name>, one for me"
#### // If no name is provided, it should default to "you"

#### // twoFer() => "One for you, one for me"
#### // twoFer("Elton") => "One for Elton, one for me"
  ```
function twoFer(name: string='you'): string{
    return `One for ${name}, one for me`
}
console.log(twoFer('Eltoon'));
console.log(twoFer());
```
##### *name: string='you'* sheyle usul bn argumente default value berilya. eger default value berilman 
##### funksiya shu *twoFer()* gornushde chagyrylsa onna ts error berer.
### 2 exercise 
// Write a isLeapyear() function that accepts a year and returns true/false depending on if the year is a leap year
// isLeapYear(2012) => true
// isLeapYear(2013) => false
### 1st version solving
```
function isLeapYear(year:number): boolean{
    if (year%4===0 && year%100!==0) return true
 else if(year % 400 === 0){
    return true;}
    else return false;
}
console.log(isLeapYear(2013))//false
console.log(isLeapYear(2012))//true
console.log(isLeapYear(2016))//true
console.log(isLeapYear(2023))//false
console.log(isLeapYear(2024))//true

```
### 2 version
```
function isLeapYear(year:number):boolean{
    return (year%4===0 && year%100!==0) || (year%400===0);
}
```

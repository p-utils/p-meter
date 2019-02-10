# P-METER - a measure of the strength of the password for node js developer ..
---
![imed-jaberi](https://scontent.ftun12-1.fna.fbcdn.net/v/t1.15752-9/51102505_2146593975378362_2929094028592939008_n.png?_nc_cat=111&_nc_ht=scontent.ftun12-1.fna&oh=783651e9c09c9bc35c9d3f8ff9361aa4&oe=5CB77F0F "imed jaberi") 
##### The purpose of this module is to analyze the password and then categorize it according to our rules mentioned in the documentation where you can view the result numerical or textual.
###### **`NOTE:`** we verify that a blank password or that there are spaces are passed to the module function .

## Installation 
---

- NPM :
```bash
$ npm install p-meter
```

## Usage 
---
 The method of use is simple and very easy ... Just follow these steps :
Step 1 : Import the module in this way .
```javascript
const passwordMeter  = require ('p-meter') ;
```
Step 2 : Enter the password to the function with the method of view you want .
```javascript
let password  = "199812+imeD";
let result = passwordMeter (password , { displayString : true , useSpace : false });
console.log(`*************\n ${result} \n*************`);
```
Step 3 : Execute method to see the result ..
```bash
$your_pc_name_with_your_directory
*************
 STRONG FORT
*************
```

###### **`NOTE:`** This example is the simplest thing to write ... for more examples you will find them in a section of exemples  .. 


## Examples
----
The result can be displayed in a two different way ( Numerical or Textual ) .. In this section we illustrate the two ways of seeing the result .. 
1 - Numerical : 
| -1 | 0 | 1 | 2 | 3 | 4 | 5 | 6 |
|----|---|---|---|---|---|---|---|

2 - Textual :
| ERROR | FAIBLE | AVG | ABOVE AVG | STRONG AVG | FORT | ABOVE FORT | STRONG FORT |
|-------|--------|-----|-----------|------------|------|------------|-------------|

## Rules : 
---
We can divide passwords into four categories (numbers, uppercase alphabet, lowercase alphabet and special characters) ..
We have 8 levels of results:
- Level 1 (-1 or ERROR): If you have an invalid password that is empty or composed of spaces.
- Level 2 (0 or LOW): If there is only one category in the password of the four.
- Level 3 (1 or AVG): if there are two categories in the password and the special characters do not belong to them.
- Level 4 (2 or ABOVE AVG): if there are two categories in the password and the special characters belong to it.
- Level 5 (3 or STRONG AVG): If you have three categories and the special characters do not belong to them.
- Level 6 (4 or FORT): If you have three categories and the special characters belong to them.
- Level 7 (5 or ABOVE FORT): if all categories are present.
- Level 8 (6 or STRONG FORT): If all categories are present with the following characteristics:
    - If uppercase letters are at least 30% of the password length, lowercase letters must be at least 10%.
    - If lowercase letters represent 30% of the length of the password, the capital letters must represent at least 10%.
    - Special characters must be at least 20%.
#### License
---
[MIT](https://choosealicense.com/licenses/mit/) 

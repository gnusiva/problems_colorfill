# problems_colorfill
This problem is to fill the color in an image with given x and y co-ordinates

```
https://codeinterview.io/DKPNLCKBEI

// Installed npm packages: jquery underscore request express
// jade shelljs passport http sys lodash async mocha chai sinon
// sinon-chai moment connect validator restify ejs ws co when
// helmet wrench brain mustache should backbone forever debug jsdom

/* 
   0. 1. 2. 3.
0 [4, 4, 5, 5]
1 [4, 3, 4, 5]
2 [4, 5, 5, 5]
3 [4, 5, 6, 6]
4 [4, 4, 7, 4]

[
 [4, 4, 5, 5]
 [4, 3, 4, 5]
 [4, 5, 5, 5]
 [4, 5, 6, 6]
 [4, 4, 7, 4]
  
]

source: 3, 1 
new color is 6
*/
var _ = require('underscore');

var evens = _.reject([1, 2, 3, 4, 5, 6], (num) => num % 2 != 0);

// console.log("Evens");
// console.log(evens);

let image = [
 [4, 4, 5, 5],
 [4, 3, 4, 5],
 [4, 5, 6, 5],
 [5, 5, 5, 6],
 [4, 5, 7, 4]
]
const xMax = image[0].length;
const yMax = image.length;

function fillColor(y, x, newColor) {
  prevColor = image[y][x];
  console.log('Previous Color:', prevColor)
  // travel rightSide
  for(let localX=x; localX<xMax; localX++) {
    if( image[y][localX] === prevColor ) {
      image[y][localX] = newColor;
    } else {
      
    }
  }
  
}

fillColor(3,0, 8);
console.log(image)

// Your last C/C++ code is saved below:
// #include <iostream>
// using namespace std;

// int main() {
// 	cout<<"Hello";
// 	return 0;
// }

```

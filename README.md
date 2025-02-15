# MongoDB $inc Operator Error
This repository demonstrates a common error when using the `$inc` operator in MongoDB. The `$inc` operator is used to increment a numerical field by a given value. However, attempting to use it with a non-numerical value will result in an error.

## Bug Description
The `bug.js` file shows an example of incorrect usage where the `count` field is attempted to be incremented by the string value '1'. This results in an error because the `$inc` operator requires a numerical value.

## Solution
The `bugSolution.js` file shows the corrected code where we explicitly convert the value to a number. We convert the string '1' to a number using parseInt() before using it with the $inc operator. 

## How to reproduce the bug
1. Create a MongoDB database and a collection (e.g. myCollection).
2. Insert a document into the collection with a numerical field (e.g. { _id: 1, count: 0 }).
3. Run the code in `bug.js`. You will observe an error.
4. Correct the code as shown in `bugSolution.js` and run it again; this should work correctly.
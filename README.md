# Envelope
Hi, welcome to the 📨 envelope 📨 API docs. This repo describes the methods you can call on the envelope object, which will give you access to the data entered in the spreadsheet tab on [envelope.li](https://envelope.li).

🚧 This documentation in under construction. 🚧

## data
type: property

status: ISSUE: should be private

description: This property may gives you all the data in the spreadsheet as an array of arrays. It can return the array in unpredictable sizes of null-arrays. Better use the method trimmedData().

example: 

`envelope.data // => [[1, 2, 3, null, null, null, null], [4, 5, 6, null, null, null, null], [null, null, null, null, null, null, null]]`

## toArrayofObjects(upperLeft, lowerRight)
type: method

status: UNFINISHED: Give example what types the arguments should be.

description: assumes the upper row to be headers of columns, and returns an array of objects with these headers as properties for each item in the array.

arguments: optional arguments that constrain the region that will be parsed. If not used, it will use all trimmed data like in the trimmedData() method.

example:

`envelope.toArrayofObjects // => [{ name: "Doug", book: "The Good Parts" }, { name: "Tommy", book: "Joe Speedboot" }]`


## trimmedData()
type: method

status: OK

description: returns the trimmed data in the spreadsheet. All rows or columns that only contain `null` or `""`, and that are not between non-null rows or columns, are deleted. 

example:

`envelope.trimmedData // => [[1, 2, 3], [4, 5, 6]]`

## version
type: property

status: OK

description: returns the version of envelope you are working with.

## _transpose()
type: method

status: ISSUE: should be public


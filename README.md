# Envelope
Hi, welcome to the envelope API docs. This repo describes the methods you can call on the envelope object, which will give you access to the data entered in the spreadsheet tab on [envelope.li](https://envelope.li).

## data
type: property

status: issue: should be private

description: This property may gives you all the data in the spreadsheet as an array of arrays. It can return the array in unpredictable sizes of null-arrays. Better use the method trimmedData().

example: 
envelope.data // => [[1, 2, 3, null, null, null, null], [4, 5, 6, null, null, null, null], [null, null, null, null, null, null, null]]

## version
type: property

description: returns the version of envelope you are working with.

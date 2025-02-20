# MongoDB $expr Query with Date Comparison Error

This repository demonstrates a common error when using the `$expr` operator with date comparisons in MongoDB.  The incorrect query fails if the field being compared is not of the correct `Date` type. The solution shows how to correctly use the `$toDate` operator to handle potential type mismatches.

## Bug Description
The original query attempts to compare a date field directly with an ISODate object using `$gt` within `$expr`. If the field isn't already a Date object, this query will result in an error. 

## Solution
The solution uses the `$toDate` operator to convert the field to a Date object before performing the comparison. This ensures the query functions correctly regardless of the field's data type.
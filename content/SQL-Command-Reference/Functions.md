---
title: "Function"
metaTitle: "Function"
metaDescription: "Function"
---

## SQL Functions

Some SQL functions for quick lookup.

## Table Of Contents

- [SQL Functions](#sql-functions)
- [Table Of Contents](#table-of-contents)
- [Types Of Functions](#types-of-functions)
- [DUAL Table In Oracle](#dual-table-in-oracle)
- [Numeric Functions](#numeric-functions)
- [Character Functions](#character-functions)
- [Date Functions](#date-functions)
- [Conversion Functions](#conversion-functions)

## Types Of Functions

Two types,

- **Single Row Functions**: Single row or Scalar functions return a value for every row that is processed in a query
- **Group Functions**: These functions group the rows of data based on the values returned by the query. This is discussed in `SQL GROUP` functions. The group functions are used to calculate aggregate values like total or average, which return just one total or one average value after processing a group of rows.

They are,

- **Numeric Functions**: These are functions that accept numeric input and return numeric values
- **Character Or Text Functions**: These are functions that accept character input and can return both character and number values.
- **Date Functions**: These are functions that take values that are of datatype DATE as input and return values of datatype DATE, except for the `MONTHS_BETWEEN` function, which returns a number.
- **Conversion Functions**: These are functions that help us to convert a value in one form to another form
  - For Example: A null value into an actual value, or a value from one datatype to another datatype like `NVL`, `TO_CHAR`, `TO_NUMBER`, `TO_DATE` etc.

You can combine more than one function together in an expression. This is known as nesting of functions.

## DUAL Table In Oracle

This is a single row and single column dummy table provided by oracle. This is used to perform mathematical calculations without using a table.

## Numeric Functions

Some are,

- ABS (x) -> Absolute value of the number 'x'
- CEIL (x) -> Integer value >= 'x'
- FLOOR (x) -> Integer value <= 'x'
- TRUNC (x, y) ->  Truncates value of number 'x' up to 'y' decimal places
- ROUND (x, y) -> Rounded off value of the number 'x' up to the number 'y' decimal places

## Character Functions

Some are,

- `LOWER`(string_value) -> All the letters in 'string_value'is converted to lowercase
- `UPPER`(string_value) -> All the letters in 'string_value'is converted to uppercase
- `INITCAP`(string_value) -> All the letters in 'string_value'is converted to mixed case
- `LTRIM`(string_value, trim_text) -> All occurrences of 'trim_text' is removed from the left of'string_value'
- `RTRIM`(string_value, trim_text) -> All occurrences of 'trim_text'from the left and right of'string_value'
- `TRIM`(trim_text FROM string_value) -> 'trim_text' can also be only one character long
- `SUBSTR`(string_value, m, n) -> Returns 'n' number of characters from 'string_value'starting from the 'm' position
- `LENGTH`(string_value) -> Number of characters in'string_value' in returned
- `LPAD`(string_value, n, pad_value) -> Returns 'string_value' left-padded with 'pad_value' . The length of the whole string will be of 'n' characters
- `RPAD`(string_value, n, pad_value) -> Returns 'string_value' right-padded with 'pad_value' . The length of the whole string will be of 'n' characters

## Date Functions

Some are,

- `ADD_MONTHS` (date, n) -> Returns a date value after adding 'n' months to the date'x'
- `MONTHS_BETWEEN` (x1, x2) -> Returns the number of months between dates x1 and x2
- `ROUND` (x, date_format) -> Returns the date 'x' rounded off to the nearest century, year, month, date, hour, minute, or second as specified by the'date_format'
- `TRUNC` (x, date_format) -> Returns the date 'x' lesser than or equal to the nearest century, year, month, date, hour, minute, or second as specified by the 'date_format'
- `NEXT_DAY` (x, week_day) -> Returns the next date of the'week_day' on or after the date 'x' occurs
- `LAST_DAY` (x) -> It is used to determine the number of days remaining in a month from the date 'x'specified
- `SYSDATE` -> Returns the systems current date and time
- `NEW_TIME` (x, zone1, zone2) -> Returns the date and time in zone2 if date 'x' represents the time in zone1

## Conversion Functions

- `TO_CHAR` (x [,y]) -> Converts Numeric and Date values to a character string value. It cannot be used for calculations since it is a string value
- `TO_DATE` (x [, date_format]) -> Converts a valid Numeric and Character values to a Date value. Date is formatted to the format specified by 'date_format'
- `NVL` (x, y) -> If 'x' is NULL, replace it with 'y'. 'x'and 'y' must be of the same datatype
- `DECODE` (a, b, c, d, e, default_value) -> Checks the value of 'a', if a = b, then returns 'c'. If a = d, then returns 'e'. Else, returns default_value

# Formulas for Import/Export

Dev note: in progress...

## SQR

A square root of `X` is a number `R` such that `R^2=X`.

Usage example:

```
Name of the function: SQR
Number of parameters: 1
Type of parameters: number

INPUT: SQR(451)
OUTPUT: 203401
```

## SIN

The sine function `SIN(X)`. `X` is a real-type expression. `SIN` returns the sine of the angle `X` in radians.

Usage example:

```
Name of the function: SIN
Number of parameters: 1
Type of parameters: number

INPUT: SIN(1)
OUTPUT: 0.84
```

## COS

The cosine function `COS(X)`. `X` is a real-type expression. `COS` returns the cosine of the angle `X` in radians.

Usage example:

```
Name of the function: COS
Number of parameters: 1
Type of parameters: number

INPUT: COS(1)
OUTPUT: 0.54
```


## ATAN

The inverse tangent function `ATAN(X)`.

Usage example:

```
Name of the function: ATAN
Number of parameters: 1
Type of parameters: number

INPUT: ATAN(1)
OUTPUT: 0.79
```

## SINH

The hyperbolic sine function `SINH(X)`.

Usage example:

```
Name of the function: SINH
Number of parameters: 1
Type of parameters: number

INPUT: SINH(1)
OUTPUT: 1.18
```

## COSH

The hyperbolic cosine function `COSH(X)`.

Usage example:

```
Name of the function: COSH
Number of parameters: 1
Type of parameters: number

INPUT: COSH(1)
OUTPUT: 1.54
```

## COTAN

The cotangent function `COTAN(X)`

Usage example:

```
Name of the function: COTAN
Number of parameters: 1
Type of parameters: number

INPUT: COTAN(1)
OUTPUT: 0.65
```

## TAN

The tangent function `TAN(X)`.

Usage example:

```
Name of the function: TAN
Number of parameters: 1
Type of parameters: number

INPUT: TAN(1)
OUTPUT: 1.56
```

## EXP

The exponential function `EXP(X)`.

Usage example:

```
Name of the function: EXP
Number of parameters: 1
Type of parameters: number

INPUT: EXP(1)
OUTPUT: 2.7183
```

## LN

The natural logarithm `LN(X)` is the logarithm having base `e`, where `e=2.718281828...`.

Usage example:

```
Name of the function: LN
Number of parameters: 1
Type of parameters: number

INPUT: LN(451)
OUTPUT: 6.11
```

## LOG

Gives the natural logarithm of X (logarithm to base 10).

Usage example:

```
Name of the function: LOG
Number of parameters: 1
Type of parameters: number

INPUT: LOG(451)
OUTPUT: 2.65
```

## SQRT

A square root of `X` is a number `R` such that `R^2=X`.

Usage example:

```
Name of the function: SQRT
Number of parameters: 1
Type of parameters: number

INPUT: SQRT(203401)
OUTPUT: 451
```

## ABS

The absolute value of a `real number` `X` is denoted `ABS(X)` and defined as the "unsigned" portion of `X`.

Usage example:

```
Name of the function: ABS
Number of parameters: 1
Type of parameters: number

INPUT: ABS(-451)
OUTPUT: 451
```

## SIGN

The sign of a `real number`, also called sgn or signum, is `-1` for a `negative` number (i.e., one with a `minus sign` `"-"`), `0` for the number `zero`, or `+1` for a `positive` number (i.e., one with a `plus sign` `"+"`).

Usage example:

```
Name of the function: SINH
Number of parameters: 1
Type of parameters: number

INPUT: SIGN(451)
OUTPUT: 1

INPUT: SIGN(-451)
OUTPUT: -1
```

## TRUNC

To truncate a `real number` is to discard its noninteger part. Truncation of a (positive) number `X` therefore corresponds to taking the `floor function` `FLOOR`.

Usage example:

```
Name of the function: TRUNC
Number of parameters: 1
Type of parameters: number

INPUT: TRUNC(-3.2)
OUTPUT: -3

INPUT: TRUNC(3.2)
OUTPUT: 3
```

## CEIL

The ceiling function `CEIL` gives the smallest `integer` `>=X`.

Usage example:

```
Name of the function: CEIL
Number of parameters: 1
Type of parameters: number

INPUT: CEIL(-3.2)
OUTPUT: 3

INPUT: CEIL(3.2)
OUTPUT: 4
```

## FLOOR

The floor function `FLOOR`, also called the greatest integer function or integer value, gives the largest `integer` less than or equal to `X`.

Usage example:

```
Name of the function: FLOOR
Number of parameters: 1
Type of parameters: number

INPUT: FLOOR(-3.2)
OUTPUT: -4

INPUT: FLOOR(3.2)
OUTPUT: 3
```

## RND

The random function `RND` generates a random number (double value) between 0 and 1.

Usage example:

```
Name of the function: RND
Number of parameters: 0
Type of parameters: number

INPUT: RND()
OUTPUT: 0.3
```

## VAL

The value function `VAL` returns the floating point numeric value of the string argument.

Usage example:

```
Name of the function: VAL
Number of parameters: 1
Type of parameters: number

INPUT: VAL("3.1")
OUTPUT: 3.1
```

## POW

ThepPower function `POW` raises Base to any power. For fractional exponents or exponents greater than MaxInt, Base must be greater than 0. 

Usage example:

```
Name of the function: POW
Number of parameters: 2
Type of parameters: number, number

INPUT: POW(451, 2)
OUTPUT: 203401
```

## LOGN

The LogN function `LOGN` returns the log base N of X.

Usage example:

```
Name of the function: LOGN
Number of parameters: 2
Type of parameters: number, number

INPUT: LOGN(10, 100)
OUTPUT: 2
```

## MIN

The minimum function `MIN` gives the smallest value of a set.

Usage example:

```
Name of the function: MIN
Number of parameters: 2
Type of parameters: number

INPUT: MIN(2, 3)
OUTPUT: 2
```

## MAX

The maximum function `MAX` gives the largest value of a set.

Usage example:

```
Name of the function: MAX
Number of parameters: 2
Type of parameters: number

INPUT: MAX(2, 3)
OUTPUT: 3
```

## MOD

The mod function `MOD` gives the remainder on division of M by N.

Usage example:

```
Name of the function: MOD
Number of parameters: 2
Type of parameters: number, number

INPUT: MOD(451, 2)
OUTPUT: 1
```

## IF

The `IF(b, case1, case2)` function provides branching capability. If `B` is not `0`, then it returns `case1`, else it returns `case2`. Behavior is similar to PHP's: `return b ? case1 : case2;`. If `b==0` then `case1` will not be Evaluated, and vice versa.

Usage example:

```
Name of the function: IF
Number of parameters: 3
Type of parameters: bool, any, any

INPUT: IF(HEIGHT, 3/HEIGHT, 3)
DESCRIPTION: Will make sure 3/HEIGHT does not cause division by zero
```

## STRLEN

The string lenght function returns the length of the string parameter.

Usage example:

```
Name of the function: STRLEN
Number of parameters: 1
Type of parameters: number

INPUT: STRLEN("ABC")
OUTPUT: 3
```

## STR

The string function return the string representation of the passed value.

Usage example:

```
Name of the function: STR
Number of parameters: 1
Type of parameters: number

INPUT: STR(451)
OUTPUT: "451"
```

## SUBSTR

The substring function return part of a string. The first parameter is the input string. Must be one character or longer. The second parameter is the start point. And the third parameter represent the lenght.

### 2nd param - start

If `start` is non-negative, the returned string will start at the `start`'th position in `string`, counting from zero. For instance, in the string `'abcdef'`, the character at position `0` is `'a'`, the character at position `2` is `'c'`, and so forth.

If `start` is negative, the returned string will start at the `start`'th character from the end of `string`.

If `string` is less than `start` characters long, `FALSE` will be returned.

### 3rd param - lenght

If `length` is given and is positive, the string returned will contain at most `length` characters beginning from `start` (depending on the length of `string`).

If `length` is given and is negative, then that many characters will be omitted from the end of `string` (after the start position has been calculated when a `start` is negative). If `start` denotes the position of this truncation or beyond, `FALSE` will be returned.

If `length` is given and is `0`, `FALSE` or `NULL`, an empty string will be returned.

If `length` is omitted, the substring starting from `start` until the end of the string will be returned.

Usage example:

```
Name of the function: SUBSTR
Number of parameters: 3
Type of parameters: string, number, number

INPUT: SUBSTR("abcdef", 0, -1)
OUTPUT: "abcde"

INPUT: SUBSTR("abcdef", 2, -1)
OUTPUT: "cde"

INPUT: SUBSTR(abcdef", 4, -4)
OUTPUT: false

INPUT: SUBSTR("abcdef", -3, -1)
OUTPUT: "de"
```

## CONCAT

The concatenation function `CONCAT` returns the concatanated strings. There is no preset limit on the number of parameters.

Usage example:

```
Name of the function: CONCAT
Number of parameters: unlimited
Type of parameters: number

INPUT: CONCAT("ABC", "DEF")
OUTPUT: "ABCDEF"
```

## TRIM

The trim function `TRIM` returns the trimmed version of the given string.

Usage example:

```
Name of the function: TRIM
Number of parameters: 1
Type of parameters: number

INPUT: TRIM(" abc  ")
OUTPUT: "abc"
```

## RTRIM

The `RTRIM` remove whitespaces from the ends of the string.

Usage example:

```
Name of the function: RTRIM
Number of parameters: 1
Type of parameters: number

INPUT: RTRIM("abc  ")
OUTPUT: "abc"

INPUT: RTRIM("  abc ")
OUTPUT: "  abc"
```

## LTRIM

The `LTRIM` remove whitespaces from the starts of the string.

Usage example:

```
Name of the function: LTRIM
Number of parameters: 1
Type of parameters: number

INPUT: LTRIM("  abc")
OUTPUT: "abc"

INPUT: LTRIM(" abc  ")
OUTPUT: "abc   "

```

## CHR

The `CHR` functions gets a character with the given ascii code.

Usage example:

```
Name of the function: CHR
Number of parameters: 1
Type of parameters: number

INPUT: CHR(65)
OUTPUT: "A"
```

## NUM

TODO: needs clarifications
tries to convert an expression to a number


Usage example:

```
Name of the function: NUM
Number of parameters: 1
Type of parameters: number

INPUT: NUM(1)
OUTPUT: 1
```

## SUM

SUM: SUM(2,3,5,...) functions returns the sum of it's arguments. There is no preset limit on the number of parameters.

Usage example:

```
Name of the function: SUM
Number of parameters: 1
Type of parameters: number

INPUT: SUM(1)
OUTPUT: 1
```

## UPPER

UPPERCASE STRING

Usage example:

```
Name of the function: UPPER
Number of parameters: 1
Type of parameters: $string

INPUT: UPPER(1)
OUTPUT: 1
```

## LOWER

lowercase string

Usage example:

```
Name of the function: LOWER
Number of parameters: 1
Type of parameters: $string

INPUT: LOWER(1)
OUTPUT: 1
```

## TITLECASE

Title Case String

Usage example:

```
Name of the function: TITLECASE
Number of parameters: 1
Type of parameters: $string

INPUT: TITLECASE(1)
OUTPUT: 1
```

## MATCH

check if strings are the same

Usage example:

```
Name of the function: MATCH
Number of parameters: 2
Type of parameters: $p1, $p2, $caseSensitve = 1

INPUT: MATCH(1, 1)
OUTPUT: 1
```

## PAD

pads a given string to given length by given char

Usage example:

```
Name of the function: PAD
Number of parameters: 3
Type of parameters: string, char, length

INPUT: PAD(1)
OUTPUT: 1
```

## DS_MAP

luminous datasource mapping

Usage example:

```
Name of the function: DS_MAP
Number of parameters: 5
Type of parameters: $input, $dataSource, $match, $output, $default

INPUT: DS_MAP(1, 1, 1, 1, 1)
OUTPUT: 1
```

## CEEB_MAP

luminous ceeb mapping

Usage example:

```
Name of the function: CEEB_MAP
Number of parameters: 4
Type of parameters: $input, $match, $output, $default

INPUT: CEEB_MAP(1, 1, 1, 1)
OUTPUT: 1
```

## CHECKBOX_FIRST

on $json_input form array, finds first item/object with checked, and returns its text field, or an empty string, if not exists.

Usage example:

```
Name of the function: CHECKBOX_FIRST
Number of parameters: 1
Type of parameters: $json_input

INPUT: CHECKBOX_FIRST(1)
OUTPUT: 1
```

## CHECKBOX_CHECKED

on $json_input form array, finds all item/object with checked, and returns its text field, concatenated by $delimiter

Usage example:

```
Name of the function: CHECKBOX_CHECKED
Number of parameters: 2
Type of parameters: $json_input, $delimiter

INPUT: CHECKBOX_CHECKED(1, 1)
OUTPUT: 1
```

## CONTAINS

is $string part of $substr?

Usage example:

```
Name of the function: CONTAINS
Number of parameters: 2
Type of parameters: $string, $substr

INPUT: CONTAINS(1, 1)
OUTPUT: 1
```

## HAS_ONE_TRUE

is $json_input cointains a truthy $attribute?

Usage example:

```
Name of the function: HAS_ONE_TRUE
Number of parameters: 2
Type of parameters: $json_input, $attribute

INPUT: HAS_ONE_TRUE(1, 1)
OUTPUT: 1
```

## STARTS_WITH

is $string starts with $substr?

Usage example:

```
Name of the function: STARTS_WITH
Number of parameters: 2
Type of parameters: $string, $substr

INPUT: STARTS_WITH(1, 1)
OUTPUT: 1
```

## ENDS_WITH

is $string ends with $substr?

Usage example:

```
Name of the function: ENDS_WITH
Number of parameters: 2
Type of parameters: $string, $substr

INPUT: ENDS_WITH(1, 1)
OUTPUT: 1
```

## LEFT

first $numChars of $string

Usage example:

```
Name of the function: LEFT
Number of parameters: 2
Type of parameters: $string, $numChars

INPUT: LEFT(1, 1)
OUTPUT: 1
```

## RIGHT

last $numChars of $string

Usage example:

```
Name of the function: RIGHT
Number of parameters: 2
Type of parameters: $string, $numChars

INPUT: RIGHT(1, 1)
OUTPUT: 1
```

## LEN

$string length

Usage example:

```
Name of the function: LEN
Number of parameters: 1
Type of parameters: $string

INPUT: LEN(1)
OUTPUT: 1
```

## SPLIT_INDEX

splits $string by $delim, and takes $index th item

Usage example:

```
Name of the function: SPLIT_INDEX
Number of parameters: 3
Type of parameters: $string, $delim, $index

INPUT: SPLIT_INDEX(1, 1, 1)
OUTPUT: 1
```

## REGEXP_MATCH

check if $string matches on $pattern. Uses php regexp

Usage example:

```
Name of the function: REGEXP_MATCH
Number of parameters: 2
Type of parameters: $string, $pattern

INPUT: REGEXP_MATCH(1)
OUTPUT: 1
```

## REGEXP_REPLACE

replaces $pattern with $replaceWith on $string. Using php regexp

Usage example:

```
Name of the function: REGEXP_REPLACE
Number of parameters: 3
Type of parameters: $string, $pattern, $replaceWith

INPUT: REGEXP_REPLACE(1)
OUTPUT: 1
```

## REGEXP_EXTRACT

finds $pattern in $string. Using php regexp

Usage example:

```
Name of the function: REGEXP_EXTRACT
Number of parameters: 2
Type of parameters: $string, $pattern

INPUT: REGEXP_EXTRACT(1, 1)
OUTPUT: 1
```

## REGEXP_EXTRACT_NTH

finds $index th match of $pattern on $string. Using php regexp

Usage example:

```
Name of the function: REGEXP_EXTRACT_NTH
Number of parameters: 3
Type of parameters: $string, $pattern, $index

INPUT: REGEXP_EXTRACT_NTH(1, 1, 1)
OUTPUT: 1
```

## DATE_ADD

adds $interval of $datePart to $date. $date should be in Y-m-d H:i:s, $interval is an integer, $datePart is second/minute/hour/day/month/year. Keeps output as Y-m-d H:i:s

Usage example:

```
Name of the function: DATE_ADD
Number of parameters: 3
Type of parameters: $datePart, $interval, $date

INPUT: DATE_ADD(1, 1, 1)
OUTPUT: 1
```

## DATE_DIFF

diff between Y-m-d H:i:s formatted $startDate and $endDate, using $datePart as unit (which is one of second/minute/hour/day/month/year)

Usage example:

```
Name of the function: DATE_DIFF
Number of parameters: 3
Type of parameters: $datePart, $startDate, $endDate

INPUT: DATE_DIFF(1, 1, 1)
OUTPUT: 1
```

## DATE_COMPARE

check if $p1 $operator $p2 true. $p1,$p2 is Y-m-d H:i:s date, $operator is <;>;<=;>=;!=;=

Usage example:

```
Name of the function: DATE_COMPARE
Number of parameters: 3
Type of parameters: $p1, $operator, $p2

INPUT: DATE_COMPARE(1, 1, 1)
OUTPUT: 1
```

## DATE_FORMAT

Reformat $input date for $format, which should be a valid php format string.

Usage example:

```
Name of the function: DATE_FORMAT
Number of parameters: 2
Type of parameters: $input, $format

INPUT: DATE_FORMAT(1, 1)
OUTPUT: 1
```

## DATE_DEFAULT

Reformat current date for $format, which should be a valid php format string.

Usage example:

```
Name of the function: DATE_DEFAULT
Number of parameters: 1
Type of parameters: $format

INPUT: DATE_DEFAULT(1)
OUTPUT: 1
```

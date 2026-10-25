# Formula Notes — Task 6

| Function | Example | When to use |
|---|---|---|
| `VLOOKUP` | `=VLOOKUP(B2,'Product Reference'!$A$2:$D$9,2,FALSE)` | Find a value in the leftmost column and return a value from a column to its right. Use `FALSE` for an exact match. |
| `XLOOKUP` | `=XLOOKUP(B2,'Product Reference'!$A$2:$A$9,'Product Reference'!$B$2:$B$9,"Not found")` | Modern lookup with separate lookup/return arrays, left/right lookup, and a not-found message. Requires Microsoft 365 or Excel 2021+. |
| `IF` | `=IF(B4>=200,"High value","Standard")` | Apply a condition and return one of two results. |
| `SUMIFS` | `=SUMIFS(Transactions!$I$2:$I$31,Transactions!$D$2:$D$31,"South",Transactions!$J$2:$J$31,"Online")` | Add sales only when multiple criteria match. |
| `COUNTIFS` | `=COUNTIFS(Transactions!$D$2:$D$31,"South",Transactions!$J$2:$J$31,"Online")` | Count rows that meet multiple conditions. |
| `LEFT` | `=LEFT(A2,3)` | Extract characters from the start of text. |
| `RIGHT` | `=RIGHT(A2,11)` | Extract characters from the end of text. |
| `MID` | `=MID(A2,5,4)` | Extract a substring from a specified starting position. |
| `TRIM` | `=TRIM(A2)` | Remove extra spaces, especially before lookups or text comparisons. |
| `CONCAT` | `=CONCAT(A2," ",B2)` | Join text values. `A2&" "&B2` is another common option. |
| `IFERROR` | `=IFERROR(VLOOKUP(A2,range,2,FALSE),"Not found")` | Replace errors with a readable fallback message. |
| `INDEX/MATCH` | `=INDEX(return_range,MATCH(lookup_value,lookup_range,0))` | Flexible lookup, useful in older Excel versions and when the return column is left of the lookup column. |

## SUMIF vs SUMIFS
- `SUMIF` supports one criterion.
- `SUMIFS` supports multiple criteria. Its first argument is the sum range.

## Edge cases to test
- Missing lookup key: use `IFERROR` or XLOOKUP's not-found argument.
- Blank input: check for `""` before looking up or classifying.
- Text vs number: `"1001"` stored as text may not match numeric `1001`.
- Extra spaces: use `TRIM`.
- Duplicate keys: a standard lookup returns one match; confirm whether duplicates are valid.
- Range mismatch: criteria ranges and sum ranges should have the same dimensions.

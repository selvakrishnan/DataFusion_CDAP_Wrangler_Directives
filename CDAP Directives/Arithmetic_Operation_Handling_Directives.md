# Arithmetic Operation Handling Directives

| Directive                                                                                  | Description                                     |
|--------------------------------------------------------------------------------------------|-------------------------------------------------|
| set-column final_column column_name_1/100                                                  | Dividing the value in a column by given value (For Eg: Divide by 100). Note to perform arithmetic operation it will work without converting datatype |
| set-column final_column  column_name_1/math:pow(10,-3)                                     | Dividing column_name_1 by 10 to the power of -3 |
| set-column final_column format("%.3f",column_name_1)                                       | To format it to 3 decimal values                |
| set-column hexadecimal_column "2A"                                                         | To convert Hexadecimal to Decimal values (Step 1) |
| set-column final_decimal_column 1.parseInt(hexadecimal_column,16)"                         | To convert Hexadecimal to Decimal values (Step 2) |
| set-column decimal_column "10"                                                             | To convert Decimal to Hexadecimal values (Step 1) |
| set-type decimal_column int                                                                | To convert Decimal to Hexadecimal values (Step 2) |
| set-column hexadecimal_column 1.toHexString(decimal_column)                                | To convert Decimal to Hexadecimal values (Step 3) |
| uppercase hexadecimal_column                                                               | To convert Decimal to Hexadecimal values (Step 4) |
| set-column :final_decimal_column exp:{new("java.math.BigDecimal", decimal_column_1 ).setScale(9)} | For decimal value set the scale to given value. Note : decimal_column -> needs to be in string datatype |

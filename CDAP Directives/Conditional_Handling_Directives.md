# Conditional Handling Directives

| Directive                                                                                                                               | Description                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| filter-rows-on condition-false (column_name1 <= column_name2) && (column_name3== null &#124;&#124; column_name1 >= column_name2) | To filter records based on given condition                           |
| find-and-replace column_name s/<find_value>/<Replace_with_new_value>/g                                                                  | To Replace a pre defined value with new value                        |
| set-column Target_column_name Source_column_name                                                                                                    | To copy values from one field to another field  or (to a new field)  |
| set-column New_column_name if(column_name1 == '0'){"Zero"} else if(column_name2 == null){column_name3} else {"NA"}                                  | Using multiple if else stmt                                          |
| set-column New_column_name if(column_name1=~ ['1','2','3'] ) {null} else {column_name2}                                                             | To compare list of values with a single field                        |
| filter-rows-on condition-false ((column_name1 == 'Pass') && (column_name2 =~ ["60","70","80","90","100"]))                     | Filter records in the given values                                   |
| set-column New_column_name column_name1 < column_name2 ?  column_name1 :  column_name2                                                              | Ternary operator way of applying filter condition                    |
| filter-rows-on condition-false (!empty(column_name1))                                                                                      | Filter records which are not empty                                   |
| filter-rows-on condition-true (column_name1 =~ ["Apple" , "Orange"])                              | column_name1 NOT IN ('Apple','Orange')|                                                                      |

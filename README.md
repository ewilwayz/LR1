# LR1_parser
This code is an LR 1 parser written by a JS script, according to the grammar below. This parser works according to the table of provisions and rules of the grammar itself.

**Grammar**
| Rules  |   |
| ------------- | ------------- |
| S ::=  | <программа>$  |
| <программа>::=  | <блок>  |
| <блок>::=  | <оператор> ;< блок >  |
| <оператор>::= | <идент>:=<выражение>  |
| <оператор>::=   | If <выражение> THEN <оператор> Endif  |
| <выражение>::=  | <фактор>|<выражение>#<фактор>  |
| <фактор>::=  | <первичное>|<фактор>&<первичное>  |
| <первичное>::=  | <идент>|<число>  |

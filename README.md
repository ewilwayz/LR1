# LR1_parser
This code is an LR1 parser, according to the grammar given below. This parser works according to the table of states and rules of the grammar itself.

**Grammar**

S ::= <программа>$
<программа>::=<блок>
<блок>::=<оператор>
<блок>::= <оператор> ;< блок >
<оператор>:=<идент>:=<выражение>
<оператор>:= If <выражение> THEN <оператор> Endif
<выражение>::=<фактор>|<выражение>#<фактор>
<фактор>::=<первичное>|<фактор>&<первичное>
<первичное>::=<идент>|<число>

Преобразованная грамматика для выполнения парсинга:
<Pr>::= 1<Bl>2
Bl::= 1<Op>3
Bl::= 1<Op>3 ; 4<Bl>5
Op::= 1<id>6 := 7<exp>8
Op::=1I9 <exp>10 T 11<Op>12 E13
exp::= 9,15<fac>14
exp::= 9,15<fac>14  # 15<exp>16
fac::= 15,18<prim>17
fac::= 15,18<prim>17 & 18<fac>19
prim::= 15,18<id>20
prim::= 15,18<digit>21
digit::= 15,18<0>22
id::= 15,18<A>23

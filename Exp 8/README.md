# Experiment 8 — Postfix Expression Evaluator (YACC + Lex)

A postfix (Reverse Polish Notation) expression evaluator built with Lex
(`postfix257.l`) for tokenizing and Yacc (`postfix257.y`) for parsing and
evaluating expressions (`+ - * /`, division-by-zero handling and syntax-error
recovery). Operands are pushed and operators are applied to the two most
recent values, so no parentheses or precedence rules are needed.
## Terminal session
```
lab-03-25@lab-03-25-OptiPlex-3280-AIO:~$ vim postfix257.l
lab-03-25@lab-03-25-OptiPlex-3280-AIO:~$ vim postfix257.y
lab-03-25@lab-03-25-OptiPlex-3280-AIO:~$ yacc -d postfix279.y
lab-03-25@lab-03-25-OptiPlex-3280-AIO:~$ lex postfix257.l
lab-03-25@lab-03-25-OptiPlex-3280-AIO:~$ gcc y.tab.c lex.yy.c -o postfix257 -ll
lab-03-25@lab-03-25-OptiPlex-3280-AIO:~$ ./postfix257
Postfix Evaluator: Enter expressions (Ctrl+C to exit)
5 4 +
Result = 9
10 20 * 5 /
Result = 40
10 0 /
Error: Division by zero
Result = 0
10+5
Syntax Error! Please re-enter.
12 50 * 95 + 10 2 / -
Result = 690
```

## Build steps
```
yacc -d postfix257.y      # generates y.tab.c and y.tab.h
lex postfix257.l          # generates lex.yy.c
gcc y.tab.c lex.yy.c -o postfix257 -ll
./postfix257
```

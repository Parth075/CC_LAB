# Experiment 2 — Lexical Analyzer

## Terminal session
```
sit-lab2-pc30@sit-lab2-pc30-OptiPlex-3280-AIO:~$ vim analyzer1257.l
sit-lab2-pc30@sit-lab2-pc30-OptiPlex-3280-AIO:~$ vim input1257.c
sit-lab2-pc30@sit-lab2-pc30-OptiPlex-3280-AIO:~$ lex analyzer1257.l
sit-lab2-pc30@sit-lab2-pc30-OptiPlex-3280-AIO:~$ gcc lex.yy.c -o analyzer1257
sit-lab2-pc30@sit-lab2-pc30-OptiPlex-3280-AIO:~$ ./analyzer1257 input1257.c
=== Lexical Analysis Results ===
Lines:        8
Spaces:       13
Words:        12
Keywords:     4
Identifiers: 5
Comments:     0
sit-lab2-pc30@sit-lab2-pc30-OptiPlex-3280-AIO:~$
```

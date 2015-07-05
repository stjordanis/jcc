# jcc
Janus Circuit Compiler 

For help use:

jcc -h 

Currently a semicolon is need after each statement.
This will hopefully be fixed when I have time to update the parser.

Not all operations are yet supported.

Due to the compilation target (no-feedback circuit model),  loops are only planned to be supported in the case where they have fixed bounds.  For the same reason although procedures might be supported in the future recursive calls will not be.

For example try: 
```
x1 x2;

if x2 < x1 then
  x1 += 15;
else
  x1 += 8;
fi x2 < x1;
x2 ^= x1;
```
# Simple Regular Expression Implimentaion


## TODO
* DONE determine optimization
* DONE label_set optimization
* DONE fsm trim

## Regex BNF
```
alpha  -> 'a'-'z' 'A'-'Z' '.'
concat -> alpha | a
          alpha '-' alpha # a-z
factor -> alpha |
          '(' alpha+ ')' |
          '[' concat ']'
expr -> factorfactor | #��������
     -> factor '*' #*����
     -> factor '+' #+����
     -> factor '|' factor #������
exprs -> expr exprs
```


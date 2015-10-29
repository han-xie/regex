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

## FSM Determine Example
look at the fsm-test.cc:test_determine() function

![FSM Determine](./img/determine.png "Determine Procedure")

![FSM Determine Result](./img/dfa.png "Determine Result DFA")

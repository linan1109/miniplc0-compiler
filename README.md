# miniplc0-compiler
<字母> ::=
     'a'|'b'|'c'|'d'|'e'|'f'|'g'|'h'|'i'|'j'|'k'|'l'|'m'|'n'|'o'|'p'|'q'|'r'|'s'|'t'|'u'|'v'|'w'|'x'|'y'|'z'
    |'A'|'B'|'C'|'D'|'E'|'F'|'G'|'H'|'I'|'J'|'K'|'L'|'M'|'N'|'O'|'P'|'Q'|'R'|'S'|'T'|'U'|'V'|'W'|'X'|'Y'|'Z'
<数字> ::= '0'|'1'|'2'|'3'|'4'|'5'|'6'|'7'|'8'|'9'
<符号> ::= '+'|'-'

<无符号整数> ::= <数字>{<数字>}
<标识符> ::= <字母>{<字母>|<数字>}

<关键字> ::= 'begin' | 'end' | 'const' | 'var' | 'print'

<程序> ::= 'begin'<主过程>'end'
<主过程> ::= <常量声明><变量声明><语句序列>

<常量声明> ::= {<常量声明语句>}
<常量声明语句> ::= 'const'<标识符>'='<常表达式>';'
<常表达式> ::= [<符号>]<无符号整数>

<变量声明> ::= {<变量声明语句>}
<变量声明语句> ::= 'var'<标识符>['='<表达式>]';'

<语句序列> ::= {<语句>}
<语句> ::= <赋值语句>|<输出语句>|<空语句>
<赋值语句> ::= <标识符>'='<表达式>';'
<输出语句> ::= 'print' '(' <表达式> ')' ';'
<空语句> ::= ';'

<表达式> ::= <项>{<加法型运算符><项>}
<项> ::= <因子>{<乘法型运算符><因子>}
<因子> ::= [<符号>]( <标识符> | <无符号整数> | '('<表达式>')' )

<加法型运算符> ::= '+'|'-'
<乘法型运算符> ::= '*'|'/'

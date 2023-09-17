# Transform-the-expression
# cook your dish here
t = int(input())
for ic in range(t):
    inp_str=input()
    operators = []
    operands = []
    output=['','','']
    len_str=len(inp_str)
    _index=0
        while(_index<len_str):
        curr_char = inp_str[_index]
        _index=_index+1
        if (curr_char == '('):
            continue
        elif curr_char in '+-*/^':
                 operators.append(curr_char)
        elif(curr_char==')'):
            #do a pop
            output[1]=(operands.pop())
            output[0]=(operands.pop())
            output[2]=(operators.pop())
            operands.append(''.join(output))
        else:
            #it's a alphabet put it in operands
            operands.append(curr_char)
    print(''.join(output))
              

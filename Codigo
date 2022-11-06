!pip install automata-lib==1.0.0.post4

def proy(numbers,password,no_pass): from automata.tm.dtm import DTM d = DTM( states={'q0', 'q1', 'q2','q3','q4','q5','q6','q7'}, input_symbols={'a','b','c','d','e','f','g','h','i','j','k','l','m','n','ñ','o','p','q','r','s','t','u','v','w','x','y','z'}, tape_symbols={'a','b','c','d','e','f','g','h','i','j','k','l','m','n','ñ','o','p','q','r','s','t','u','v','w','x','y','z', '1','2','3','4','5','6','7','8','9','0','B'}, transitions={ 'q0': { numbers[0]: ('q1', '1', 'R'), numbers[1]: ('q1', '2', 'R'), numbers[2]: ('q1', '3', 'R'), numbers[3]: ('q1', '4', 'R'), numbers[4]: ('q1', '5', 'R'), numbers[5]: ('q1', '6', 'R'), numbers[6]: ('q1', '7', 'R'), numbers[7]: ('q1', '8', 'R'), numbers[8]: ('q1', '9', 'R'), numbers[9]: ('q1', '0', 'R'), }, 'q1': { numbers[0]: ('q1', '1', 'R'), numbers[1]: ('q1', '2', 'R'), numbers[2]: ('q1', '3', 'R'), numbers[3]: ('q1', '4', 'R'), numbers[4]: ('q1', '5', 'R'), numbers[5]: ('q1', '6', 'R'), numbers[6]: ('q1', '7', 'R'), numbers[7]: ('q1', '8', 'R'), numbers[8]: ('q1', '9', 'R'), numbers[9]: ('q1', '0', 'R'),
'B': ('q2', 'B', 'L'), }, 'q2': { password[3]: ('q3',password[3], 'L'), password[0]: ('q6',password[0], 'L'), password[1]: ('q6',password[1], 'L'), password[2]: ('q6',password[2], 'L'), no_pass[0]: ('q6',no_pass[0], 'L'), no_pass[1]: ('q6',no_pass[1], 'L'), no_pass[2]: ('q6',no_pass[2], 'L'), no_pass[3]: ('q6',no_pass[3], 'L'), no_pass[4]: ('q6',no_pass[4], 'L'), no_pass[5]: ('q6',no_pass[5], 'L'), }, 'q3': { password[2]: ('q4',password[2], 'L'), password[0]: ('q6',password[0], 'L'), password[1]: ('q6',password[1], 'L'), password[3]: ('q6',password[3], 'L'), no_pass[0]: ('q6',no_pass[0], 'L'), no_pass[1]: ('q6',no_pass[1], 'L'), no_pass[2]: ('q6',no_pass[2], 'L'), no_pass[3]: ('q6',no_pass[3], 'L'), no_pass[4]: ('q6',no_pass[4], 'L'), no_pass[5]: ('q6',no_pass[5], 'L'), }, 'q4': { password[1]: ('q5',password[1], 'L'), password[0]: ('q6',password[0], 'L'), password[3]: ('q6',password[3], 'L'), password[2]: ('q6',password[2], 'L'), no_pass[0]: ('q6',no_pass[0], 'L'), no_pass[1]: ('q6',no_pass[1], 'L'), no_pass[2]: ('q6',no_pass[2], 'L'), no_pass[3]: ('q6',no_pass[3], 'L'), no_pass[4]: ('q6',no_pass[4], 'L'), no_pass[5]: ('q6',no_pass[5], 'L'), }, 'q5': { password[0]: ('q7',password[0], 'L'), password[3]: ('q6',password[3], 'L'), password[1]: ('q6',password[1], 'L'), password[2]: ('q6',password[2], 'L'), no_pass[0]: ('q6',no_pass[0], 'L'), no_pass[1]: ('q6',no_pass[1], 'L'), no_pass[2]: ('q6',no_pass[2], 'L'), no_pass[3]: ('q6',no_pass[3], 'L'), no_pass[4]: ('q6',no_pass[4], 'L'), no_pass[5]: ('q6',no_pass[5], 'L'), }

    },
    initial_state='q0',
    blank_symbol='B',
    final_states={'q6','q7'}
)
return d

import random
import pandas as pd number = ['a','b','c','d','e','f','g','h','i','j','k','l','m','n','ñ','o','p','q','r','s','t','u','v','w','x','y','z'] random.shuffle(number)

digits=['1','2','3','4','5','6','7','8','9','0']

print(" _________________________________________________") print("| | | | | |") print("| ", end = '') for i in range(10):

print( digits[i]+': '+str(number[i]), end = ' | ')

if (i+1)%5==0 and i<9: print("\n|||||_________|") print( "| | | | | |") print('| ', end = '')

print("\n|||||_________|\n") no_pass = digits password=['1','2','3','4'] no_pass.remove(password[0]) no_pass.remove(password[1]) no_pass.remove(password[2]) no_pass.remove(password[3])

print('PD: La contraseña correcta es 1234') clave='' while len(clave)!=4: print("Ingrese Contraseña") clave = input()

result = proy(number,password,no_pass) word = result.validate_input(clave, step=False) if word[0]=='q6': print('Contraseña Incorrecta!') elif word[0]=='q7': print('Contraseña Correcta')

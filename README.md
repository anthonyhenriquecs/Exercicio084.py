# Exercicio084.py

temp = []
princ = []
mai = men = 0
while True:
    temp.append(str(input('Nome:')))
    temp.append(float(input('Peso:')))
    if len(princ) == 0:
        mai = men = temp[1]
    else:
        if temp[1] > mai:
            mai = temp[1]
        elif temp[1] < men:
            men = temp[1]
    princ.append(temp[:])
    temp.clear()
    resp = str(input('Quer continuar? [S/N]'))
    if resp in 'Nn':
        break
print('-='*30)
print(f'Os dados informados foram: {princ}')
print(f'Ao todo voce cadastrou {len(princ)} pessoas')
for p in princ:
    if p[1] == mai:
        print(f'{p[0]}')
print(f'O maior peso foi de {mai}Kg. e o menor foi de {men}Kg.')

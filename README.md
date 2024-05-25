jogador1 = input("Digite o nome do jogador 1: ")
jogador2 = input("Digite o nome do jogador 2: ")
print("Segue as regras para o jogo:\nDigite 1 para pedra\nDigite 2 para papel\nDigite 3 para tesoura")
jogadasj1 = [0,0,0]
jogadasj2 = [0,0,0]
placarj1 = 0
placarj2 = 0 
for c in range(0,3,1):
    jogadasj1[c] = int(input(f'Rodada {c+1} do jogador {jogador1}: '))
    if jogadasj1[c] <1 or jogadasj1[c]>3:
        while jogadasj1[c]<1 or jogadasj1[c]>3:
            print('número inválido! Tente outra vez')
            jogadasj1[c] = int(input(f'Rodada {c+1} do jogador {jogador1}: '))

    jogadasj2[c] = int(input(f'Rodada {c+1} do jogador {jogador2}: '))
    if jogadasj1[c] <1 or jogadasj1[c]>3:
        while jogadasj1[c]<1 or jogadasj1[c]>3:
            print('número inválido! Tente outra vez')
            jogadasj1[c] = int(input(f'Rodada {c+1} do jogador {jogador1}: '))

for c in range(0,3,1):
    print(f"Resultado rodada {c+1}")
    #condições para o jogador 1 ganhar
    if jogadasj1[c] == 1 and jogadasj2[c]==3:
        print(f'{jogador1} - pedra x {jogador2} - tesoura')
        print(f'{jogador1} ganhou')
        placarj1 += 1
    elif jogadasj1[c] == 2 and jogadasj2[c]==1:
        print(f'{jogador1} - papel x {jogador2} - pedra')
        print(f'{jogador1} ganhou')
        placarj1 += 1
    elif jogadasj1[c] == 3 and jogadasj2[c]==2:
        print(f'{jogador1} - tesoura x {jogador2} - papel')
        print(f'{jogador1} ganhou')
        placarj1 += 1

  
    if jogadasj1[c] == 3 and jogadasj2[c]==1:
        print(f'{jogador1} - tesoura x {jogador2} - pedra')
        print(f'{jogador2} ganhou')
        placarj2 += 1
    elif jogadasj1[c] == 1 and jogadasj2[c]==2:
        print(f'{jogador1} - pedra x {jogador2} - papel')
        print(f'{jogador2} ganhou')
        placarj2 += 1
    elif jogadasj1[c] == 2 and jogadasj2[c]==3:
        print(f'{jogador1} - papel x {jogador2} - tesoura')
        print(f'{jogador2} ganhou')
        placarj2 += 1

  
    if placarj1 == 2 or placarj2 == 2:
        break
print(f"Placar final: {jogador1} {placarj1} x {placarj2} {jogador2}")

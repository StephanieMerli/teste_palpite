# teste_palpite
# computador joga em primeiro lugar
# um não sabe o número que o outro player jogou
# se jogar um número inferior, perde
# apresentar quantas vezes cada um jogou e quem ganhou

import random

palpite_computador = [0, ]
palpite_jogador = [0, ]
vitorias_computador = 0
vitorias_jogador = 0

while True:
    numero = random.randint(0, 100)
    palpite_computador.append(numero)

    if palpite_computador [+1] <= palpite_jogador [-1]:
        print(f"Palpite computador: {palpite_computador}")

        palpite_jogador [-1] <= palpite_computador [-1]


# Resolução do professor
jogadas = []
vitoria = "computador"
 
print("Turno do Computador")
num_computador = random.randint(1, 100)
num_utilizador = int(input("Introduza um número\n"))
jogadas.append(num_computador)
jogadas.append(num_utilizador)
 
while num_utilizador > num_computador or num_utilizador - num_computador > 99:
    print("Turno do Computador")
    num_computador = random.randint(num_computador + 50, num_computador + 150)
    jogadas.append(num_computador)
    if num_computador <= num_utilizador or num_computador - num_utilizador > 99:
        vitoria = "utilizador"
        break
    num_utilizador = int(input("Introduza um número\n"))
    jogadas.append(num_utilizador)
 
 
if vitoria == "computador":
    print(f"Ganhou o computador, o último palpite foi {num_computador} e o último palpite do utilizador foi {num_utilizador}")
elif vitoria == "utilizador":
    print(f"Ganhou o utilizador, o último palpite foi {num_utilizador} e o último palpite do computador foi {num_computador}")

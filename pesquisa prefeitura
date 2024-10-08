# Leonardo Araujo, João Filipe

import os
os.system("cls || clear")

from dataclasses import dataclass

@dataclass
class Habitantes:
    salario: float
    idade: int
    sexo: str


# Variáveis
feminino = 0
masculino = 0
contador_mulheres = 0
contador_habitantes = 0
contador_mulher5000 = 0

# Listas para armazenar dados
lista_salarial = []
lista_idade = []
lista_habitantes = []


while True:
    print("""
    1 | Adicionar pessoa1
    2 | Exibir resultados
    3 | Sair
    """)
    menu = input("Escolha uma opção: ")
    match menu:
        case "1":
            os.system("cls || clear")
            idade = int(input("Digite sua idade: "))
            sexo = input("Digite (M) para masculino ou (F) para feminino: ").upper()
            salario = float(input("Digite o seu salário: "))

            habitante = Habitantes(salario=salario, idade=idade, sexo=sexo)

            #adicionando dados às listas.
            lista_salarial.append(habitante.salario)
            lista_habitantes.append(habitante)
            lista_idade.append(habitante.idade)

            #contando mulheres com salário acima de 5000.
            if habitante.salario > 5000 and habitante.sexo == "F":
                contador_mulher5000 += 1

            #gravar dados no arquivo.
            with open("pesquisa_habitantes.txt", "a") as file:
                file.write(f"{habitante.idade},{habitante.sexo},{habitante.salario}\n")

        case "2":
            print("EXIBINDO RESULTADOS!")
            
            if lista_salarial:  #veerifica se a lista não está vazia.
                total_habitantes = len(lista_salarial)
                total_salario = sum(lista_salarial)
                media_salarial = total_salario / total_habitantes
                maior_idade = max(lista_idade)
                menor_idade = min(lista_idade)

                print(f"Média de salário do grupo é de: R$ {media_salarial:.2f}")
                print(f"Maior idade do grupo: {maior_idade}")
                print(f"Menor idade do grupo: {menor_idade}")
                print(f"Quantidade de mulheres com salário a partir de 5Mil R$: {contador_mulher5000} ")
            else:
                print("Nenhum dado cadastrado.")

        case "3":
            print("Adeus, mundo!")
            break

# softwareSensoPython

quantidadePessoas = 0
somaSalarios = 0.0
somaFilhos = 0
quantidadePessoasBaixoSalario = 0
maiorSalario = 0.0
menorSalario = 0.0
nomeMaiorSalario = ""
nomeMenorSalario = ""

while(True): #loop infinito!
    nome = input("Digite seu nome: ")
    salario = float(input("Digite o salário: "))

    if (salario < 0):
        print("Salário NEGATIVO!")
        break

    quantidadeFilhos = int(input("Digite o número de filhos: "))
    
    if (quantidadePessoas == 0):
        maiorSalario = salario
        menorSalario = salario
        nomeMaiorSalario = nome
        nomeMenorSalario = nome

    quantidadePessoas += 1
    somaSalarios += salario
    somaFilhos += quantidadeFilhos

    if (salario <= 1500):
        quantidadePessoasBaixoSalario += 1

    if (salario > maiorSalario):
        maiorSalario = salario
        nomeMaiorSalario = nome
    
    if (salario < menorSalario):
        menorSalario = salario
        nomeMenorSalario = nome


mediaSalarios = somaSalarios / quantidadePessoas
print("A média dos salários é: ", mediaSalarios)

mediaFilhos = somaFilhos / quantidadePessoas
print("A média de filhos por pessoa é: ", mediaFilhos)

porcentagemBaixoSalario = (quantidadePessoasBaixoSalario * 100) / quantidadePessoas
print("A Porcentagem de pessoas com salário abaixo de R$1.500,00 é: ", porcentagemBaixoSalario, "%")

print("Maior salário: ", maiorSalario, "Pertencente à: ", nomeMaiorSalario)
print("Menor salário: ", menorSalario, "Pertencente à: ", nomeMenorSalario)

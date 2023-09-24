# Funcao_calculador_While
Código em Python com função calculadora com entrada e saída de dados, com laço de repetição while

#FUNÇÃO CALCULADORA - AUTOR: PAULO SOUSA
#Faça uma função calculadora que os números e as operações serão feitas 
#pelo usuário. O código deve ficar rodando infinitamente até que o usuário 
#escolha a opção de sair. No início, o programa 
#mostrará a seguinte lista de operações:

#1: Soma
#2: Subtração
#3: Multiplicação
#4: Divisão
#0: Sair

#Digite o número para a operação correspondente e caso o usuário 
#introduza qualquer outro, o sistema deve mostrar a mensagem 
#“Essa opção não existe” e voltar ao menu de opções.

#Após a seleção, o sistema deve pedir para o usuário inserir 
#o primeiro e segundo valor, um de cada. Depois precisa executar 
#a operação e mostrar o resultado na tela. 
#Quando o usuário escolher a opção “Sair”, o sistema irá parar.

#É necessário que o sistema mostre as opções sempre que finalizar
# uma operação e mostrar o resultado. 

def soma(a, b):
    return a + b

def subtracao(a, b):
    return a - b

def multiplicacao(a, b):
    return a * b

def divisao(a, b):
    if b == 0:
        return "Erro! Divisão por zero. "
    return a / b

while True:
    print("Escolha a operação desejada:")
    print("1: Soma")
    print("2: Subtração")
    print("3: Multiplicação")
    print("4: Divisão")
    print("0: Sair")

    operacao = input("Digite o número da operação desejada: ")

    if operacao == "0":
        print("Processo Encerrado.")
        break
    elif operacao  not in ["1", "2", "3", "4"]:
        print("Operação inexistente.")
        continue

    num1 = int(input("Digite o primeiro número: "))
    num2 = int(input("Digite o segundo número: "))

    if operacao == "1":
        resultado = soma(num1, num2)
    elif operacao == "2":
        resultado = subtracao(num1, num2)
    elif operacao == "3":
        resultado = multiplicacao(num1, num2)
    elif operacao == "4":
        resultado = divisao(num1, num2)

    print(f"Resultado: {resultado}")


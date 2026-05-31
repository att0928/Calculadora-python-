# Calculadora-python-
Calculadora simples.
def somar(a, b):
    return a + b

def subtrair(a, b):
    return a - b

def multiplicar(a, b):
    return a * b

def dividir(a, b):
    if b == 0:
        return "Erro: não é possível dividir por zero!"
    return a / b

def exibir_menu():
    print("\n" + "=" * 40)
    print("         🧮  CALCULADORA  🧮")
    print("=" * 40)
    print("  [1]  Soma          (+)")
    print("  [2]  Subtração     (-)")
    print("  [3]  Multiplicação (×)")
    print("  [4]  Divisão       (÷)")
    print("  [0]  Sair")
    print("=" * 40)

def obter_numero(mensagem):
    while True:
        try:
            return float(input(mensagem))
        except ValueError:
            print("⚠️  Digite um número válido!")

def main():
    print("\nBem-vindo à Calculadora!")

    while True:
        exibir_menu()
        opcao = input("\nEscolha uma opção: ").strip()

        if opcao == "0":
            print("\nAté logo! 👋\n")
            break

        if opcao not in ["1", "2", "3", "4"]:
            print("⚠️  Opção inválida! Tente novamente.")
            continue

        a = obter_numero("Digite o primeiro número: ")
        b = obter_numero("Digite o segundo número: ")

        if opcao == "1":
            resultado = somar(a, b)
            operacao = "+"
        elif opcao == "2":
            resultado = subtrair(a, b)
            operacao = "-"
        elif opcao == "3":
            resultado = multiplicar(a, b)
            operacao = "×"
        elif opcao == "4":
            resultado = dividir(a, b)
            operacao = "÷"

        print(f"\n✅  {a} {operacao} {b} = {resultado}")

if __name__ == "__main__":
    main()
    

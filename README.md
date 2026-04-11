# Sistema-Bancario
Nesse repositório foi desenvolvido um codigo que se parece com um sistema de software bancario.
saldo = float(input("Digite o saldo inicial: R$ "))

while True:
    print("\n--- MENU ---")
    print("1 - Consultar saldo")
    print("2 - Sacar valor")
    print("3 - Depositar valor")
    print("4 - Sair")

    opcao = input("Escolha uma opção: ")

    if opcao == "1":
        print(f"Saldo atual: R$ {saldo:.2f}")

    elif opcao == "2":
        valor = float(input("Digite o valor do saque: R$ "))

        if valor > saldo:
            print("Saldo insuficiente ❌")
        elif valor <= 0:
            print("Valor inválido ❌")
        else:
            saldo -= valor
            print(f"Saque realizado! Novo saldo: R$ {saldo:.2f}")

    elif opcao == "3":
        valor = float(input("Digite o valor do depósito: R$ "))

        if valor <= 0:
            print("Valor inválido ❌")
        else:
            saldo += valor
            print(f"Depósito realizado! Novo saldo: R$ {saldo:.2f}")

    elif opcao == "4":
        print("Saindo do sistema...")
        break

    else:
        print("Opção inválida ❌")

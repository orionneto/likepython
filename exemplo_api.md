Exemplo simples de uma API REST para gestão de quartos de hotel em Python, utilizando apenas funções, `if`, `while`, `for` e dicionários para armazenar os dados dos quartos.

```python
# Dicionário para armazenar os quartos do hotel
quartos = {
    '101': {'tipo': 'simples', 'preco': 100, 'disponivel': True},
    '102': {'tipo': 'duplo', 'preco': 150, 'disponivel': True},
    '103': {'tipo': 'luxo', 'preco': 200, 'disponivel': True}
}

# Função para listar todos os quartos disponíveis
def listar_quartos_disponiveis():
    quartos_disponiveis = []
    for numero, quarto in quartos.items():
        if quarto['disponivel']:
            quartos_disponiveis.append({'numero': numero, 'tipo': quarto['tipo'], 'preco': quarto['preco']})
    return quartos_disponiveis

# Função para reservar um quarto
def reservar_quarto(numero):
    if numero in quartos and quartos[numero]['disponivel']:
        quartos[numero]['disponivel'] = False
        return f"Quarto {numero} reservado com sucesso!"
    else:
        return "Quarto indisponível ou inexistente."

# Função para liberar um quarto
def liberar_quarto(numero):
    if numero in quartos and not quartos[numero]['disponivel']:
        quartos[numero]['disponivel'] = True
        return f"Quarto {numero} liberado com sucesso!"
    else:
        return "Quarto já está disponível ou inexistente."

# Simulação de uma API REST usando as funções acima
def api_rest():
    while True:
        print("\nBem-vindo à API de gestão de quartos de hotel!")
        print("1. Listar quartos disponíveis")
        print("2. Reservar quarto")
        print("3. Liberar quarto")
        print("4. Sair")

        opcao = input("\nEscolha uma opção: ")

        if opcao == '1':
            quartos_disponiveis = listar_quartos_disponiveis()
            print("\nQuartos disponíveis:")
            for quarto in quartos_disponiveis:
                print(f"Número: {quarto['numero']}, Tipo: {quarto['tipo']}, Preço: R${quarto['preco']}")
        elif opcao == '2':
            numero = input("Digite o número do quarto que deseja reservar: ")
            print(reservar_quarto(numero))
        elif opcao == '3':
            numero = input("Digite o número do quarto que deseja liberar: ")
            print(liberar_quarto(numero))
        elif opcao == '4':
            print("Saindo...")
            break
        else:
            print("Opção inválida. Por favor, escolha uma opção válida.")

# Execução da API
api_rest()
```

Neste exemplo, criamos uma API REST simulada para gestão de quartos de hotel. As funções `listar_quartos_disponiveis`, `reservar_quarto` e `liberar_quarto` realizam operações relacionadas à listagem de quartos disponíveis, reserva e liberação de quartos, respectivamente. A função `api_rest` serve como ponto de entrada da API, apresentando um menu de opções para o usuário escolher. As operações são realizadas com base nas escolhas do usuário e utilizando as estruturas `if`, `while`, `for` e o dicionário `quartos` para armazenar os dados dos quartos.



1. **Definição do Dicionário de Quartos**:
```python
quartos = {
    '101': {'tipo': 'simples', 'preco': 100, 'disponivel': True},
    '102': {'tipo': 'duplo', 'preco': 150, 'disponivel': True},
    '103': {'tipo': 'luxo', 'preco': 200, 'disponivel': True}
}
```
Nesta seção, criamos um dicionário chamado `quartos` para armazenar informações sobre os quartos do hotel. Cada chave do dicionário é o número do quarto e o valor é outro dicionário contendo informações como tipo, preço e disponibilidade do quarto.

2. **Função para Listar Quartos Disponíveis**:
```python
def listar_quartos_disponiveis():
    quartos_disponiveis = []
    for numero, quarto in quartos.items():
        if quarto['disponivel']:
            quartos_disponiveis.append({'numero': numero, 'tipo': quarto['tipo'], 'preco': quarto['preco']})
    return quartos_disponiveis
```
A função `listar_quartos_disponiveis` percorre o dicionário de quartos e cria uma lista contendo os quartos disponíveis, ou seja, aqueles em que o valor da chave `disponivel` é `True`. A função retorna essa lista de quartos disponíveis.

3. **Função para Reservar um Quarto**:
```python
def reservar_quarto(numero):
    if numero in quartos and quartos[numero]['disponivel']:
        quartos[numero]['disponivel'] = False
        return f"Quarto {numero} reservado com sucesso!"
    else:
        return "Quarto indisponível ou inexistente."
```
A função `reservar_quarto` verifica se o número do quarto fornecido está no dicionário de quartos e se o quarto está disponível para reserva. Se sim, atualiza o valor da chave `disponivel` para `False` e retorna uma mensagem de sucesso. Caso contrário, retorna uma mensagem de erro.

4. **Função para Liberar um Quarto**:
```python
def liberar_quarto(numero):
    if numero in quartos and not quartos[numero]['disponivel']:
        quartos[numero]['disponivel'] = True
        return f"Quarto {numero} liberado com sucesso!"
    else:
        return "Quarto já está disponível ou inexistente."
```
A função `liberar_quarto` verifica se o número do quarto fornecido está no dicionário de quartos e se o quarto não está disponível (ou seja, já foi reservado). Se sim, atualiza o valor da chave `disponivel` para `True` e retorna uma mensagem de sucesso. Caso contrário, retorna uma mensagem de erro.

5. **Simulação da API REST**:
```python
def api_rest():
    while True:
        print("\nBem-vindo à API de gestão de quartos de hotel!")
        print("1. Listar quartos disponíveis")
        print("2. Reservar quarto")
        print("3. Liberar quarto")
        print("4. Sair")

        opcao = input("\nEscolha uma opção: ")

        if opcao == '1':
            quartos_disponiveis = listar_quartos_disponiveis()
            print("\nQuartos disponíveis:")
            for quarto in quartos_disponiveis:
                print(f"Número: {quarto['numero']}, Tipo: {quarto['tipo']}, Preço: R${quarto['preco']}")
        elif opcao == '2':
            numero = input("Digite o número do quarto que deseja reservar: ")
            print(reservar_quarto(numero))
        elif opcao == '3':
            numero = input("Digite o número do quarto que deseja liberar: ")
            print(liberar_quarto(numero))
        elif opcao == '4':
            print("Saindo...")
            break
        else:
            print("Opção inválida. Por favor, escolha uma opção válida.")
```

# Explicação Código:

Claro! Vamos analisar o código em detalhes:

1. **Definição do Dicionário de Quartos**:
```python
quartos = {
    '101': {'tipo': 'simples', 'preco': 100, 'disponivel': True},
    '102': {'tipo': 'duplo', 'preco': 150, 'disponivel': True},
    '103': {'tipo': 'luxo', 'preco': 200, 'disponivel': True}
}
```
Nesta seção, criamos um dicionário chamado `quartos` para armazenar informações sobre os quartos do hotel. Cada chave do dicionário é o número do quarto e o valor é outro dicionário contendo informações como tipo, preço e disponibilidade do quarto.

2. **Função para Listar Quartos Disponíveis**:
```python
def listar_quartos_disponiveis():
    quartos_disponiveis = []
    for numero, quarto in quartos.items():
        if quarto['disponivel']:
            quartos_disponiveis.append({'numero': numero, 'tipo': quarto['tipo'], 'preco': quarto['preco']})
    return quartos_disponiveis
```
A função `listar_quartos_disponiveis` percorre o dicionário de quartos e cria uma lista contendo os quartos disponíveis, ou seja, aqueles em que o valor da chave `disponivel` é `True`. A função retorna essa lista de quartos disponíveis.

3. **Função para Reservar um Quarto**:
```python
def reservar_quarto(numero):
    if numero in quartos and quartos[numero]['disponivel']:
        quartos[numero]['disponivel'] = False
        return f"Quarto {numero} reservado com sucesso!"
    else:
        return "Quarto indisponível ou inexistente."
```
A função `reservar_quarto` verifica se o número do quarto fornecido está no dicionário de quartos e se o quarto está disponível para reserva. Se sim, atualiza o valor da chave `disponivel` para `False` e retorna uma mensagem de sucesso. Caso contrário, retorna uma mensagem de erro.

4. **Função para Liberar um Quarto**:
```python
def liberar_quarto(numero):
    if numero in quartos and not quartos[numero]['disponivel']:
        quartos[numero]['disponivel'] = True
        return f"Quarto {numero} liberado com sucesso!"
    else:
        return "Quarto já está disponível ou inexistente."
```
A função `liberar_quarto` verifica se o número do quarto fornecido está no dicionário de quartos e se o quarto não está disponível (ou seja, já foi reservado). Se sim, atualiza o valor da chave `disponivel` para `True` e retorna uma mensagem de sucesso. Caso contrário, retorna uma mensagem de erro.

5. **Simulação da API REST**:
```python
def api_rest():
    while True:
        print("\nBem-vindo à API de gestão de quartos de hotel!")
        print("1. Listar quartos disponíveis")
        print("2. Reservar quarto")
        print("3. Liberar quarto")
        print("4. Sair")

        opcao = input("\nEscolha uma opção: ")

        if opcao == '1':
            quartos_disponiveis = listar_quartos_disponiveis()
            print("\nQuartos disponíveis:")
            for quarto in quartos_disponiveis:
                print(f"Número: {quarto['numero']}, Tipo: {quarto['tipo']}, Preço: R${quarto['preco']}")
        elif opcao == '2':
            numero = input("Digite o número do quarto que deseja reservar: ")
            print(reservar_quarto(numero))
        elif opcao == '3':
            numero = input("Digite o número do quarto que deseja liberar: ")
            print(liberar_quarto(numero))
        elif opcao == '4':
            print("Saindo...")
            break
        else:
            print("Opção inválida. Por favor, escolha uma opção válida.")
```
A função `api_rest` é a parte principal do código. Ela simula uma API REST com um loop `while` que exibe um menu de opções para o usuário. Dependendo da opção escolhida pelo usuário, as funções correspondentes são chamadas para listar quartos disponíveis, reservar um quarto, liberar um quarto ou sair do programa.

Essa é uma maneira simplificada de criar uma API REST em Python usando apenas funções, `if`, `while`, `for` e dicionários.

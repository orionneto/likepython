### If Statement (Declaração If)

O `if` é uma declaração condicional em Python que permite executar determinado bloco de código somente se uma condição for verdadeira. 

#### Exemplo Simples:
```python
# Verifica se o preço do item é superior a 100
preco = 120
if preco > 100:
    print("Este item é caro!")
```

#### Exemplo Intermediário:
```python
# Verifica se o nome do item é "Toalhas" e imprime uma mensagem correspondente
nome_item = "Toalhas"
if nome_item == "Toalhas":
    print("Toalhas são fornecidas gratuitamente.")
else:
    print("Este item não é fornecido gratuitamente.")
```

#### Exemplo Avançado:
```python
# Verifica se o item está disponível no estoque e imprime uma mensagem correspondente
estoque = {"Toalhas": 10, "Sabonetes": 5, "Shampoo": 0}
item = "Shampoo"
if item in estoque and estoque[item] > 0:
    print(f"{item} está disponível no estoque.")
else:
    print(f"{item} não está disponível no momento.")
```

### For Loop (Laço For)

O `for` é usado para iterar sobre uma sequência (como uma lista, tupla, dicionário, etc.) e executar um bloco de código para cada elemento dessa sequência.

#### Exemplo Simples:
```python
# Itera sobre uma lista de itens e os imprime
itens = ["Toalhas", "Sabonetes", "Shampoo"]
for item in itens:
    print(item)
```

#### Exemplo Intermediário:
```python
# Itera sobre um dicionário de itens e seus preços e os imprime
itens_precos = {"Toalhas": 10, "Sabonetes": 5, "Shampoo": 8}
for item, preco in itens_precos.items():
    print(f"{item}: R${preco}")
```

#### Exemplo Avançado:
```python
# Itera sobre uma lista de itens e verifica se algum item está em falta no estoque
itens_faltantes = ["Toalhas", "Shampoo", "Pasta de Dente"]
estoque = {"Toalhas": 10, "Sabonetes": 5, "Shampoo": 0}
for item in itens_faltantes:
    if item not in estoque or estoque[item] == 0:
        print(f"{item} está em falta no estoque.")
```

### While Loop (Laço While)

O `while` é usado para repetir um bloco de código enquanto uma condição especificada for verdadeira.

#### Exemplo Simples:
```python
# Imprime números de 1 a 5 usando um loop while
num = 1
while num <= 5:
    print(num)
    num += 1
```

#### Exemplo Intermediário:
```python
# Simula um contador de estoque até que um item específico esteja disponível
item = "Shampoo"
estoque = {"Toalhas": 10, "Sabonetes": 5, "Shampoo": 0}
while estoque[item] == 0:
    print(f"Estoque de {item} esgotado. Aguardando reposição.")
    # Aqui poderia ser adicionada uma lógica para repor o estoque automaticamente
    # Mas vamos simular manualmente para este exemplo:
    estoque[item] = int(input(f"Quantidade de {item} reposta: "))
print(f"{item} agora está disponível no estoque.")
```

#### Exemplo Avançado:
```python
# Simula um sistema de reserva de quartos até que todos os quartos estejam ocupados
quartos_disponiveis = 5
while quartos_disponiveis > 0:
    print(f"{quartos_disponiveis} quartos disponíveis.")
    reserva = input("Deseja reservar um quarto? (s/n): ")
    if reserva.lower() == 's':
        quartos_disponiveis -= 1
        print("Quarto reservado com sucesso!")
    else:
        print("Próximo cliente.")
print("Todos os quartos estão ocupados.")
```

Estes exemplos devem lhe dar uma compreensão básica, intermediária e avançada de como usar `if`, `for` e `while` em Python, aplicados ao contexto de cadastro de itens em um hotel.

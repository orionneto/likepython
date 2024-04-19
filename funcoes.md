
### Funções em Python:

Em Python, as funções são blocos de código reutilizáveis que realizam uma tarefa específica. Elas ajudam a organizar o código, melhorar a legibilidade e evitar repetição. As funções em Python são definidas usando a palavra-chave `def`, seguida pelo nome da função e, opcionalmente, parâmetros entre parênteses. Aqui está um exemplo simples:

```python
def saudacao(nome):
    print("Olá,", nome)

saudacao("João")  # Saída: Olá, João
```

### Funções Lambda em Python:

As funções lambda, também conhecidas como funções anônimas, são pequenas funções definidas sem nome usando a palavra-chave `lambda`. Elas são úteis quando você precisa de uma função por um curto período de tempo ou quando deseja passar uma função como argumento para outra função. Aqui está um exemplo simples:

```python
dobro = lambda x: x * 2
print(dobro(5))  # Saída: 10
```

### Aplicação ao Cadastro de Itens em um Hotel:

Vamos criar um exemplo onde usaremos funções para gerenciar o cadastro de itens em um hotel. Usaremos funções para adicionar itens, remover itens e listar todos os itens cadastrados.

#### Exemplo Simples:

```python
itens_hotel = []

def adicionar_item(item):
    itens_hotel.append(item)

def remover_item(item):
    itens_hotel.remove(item)

def listar_itens():
    print("Itens do hotel:")
    for item in itens_hotel:
        print("-", item)

adicionar_item("Toalha")
adicionar_item("Sabonete")
listar_itens()
```

#### Exemplo Intermediário:

Vamos adicionar a capacidade de adicionar informações adicionais aos itens, como preço e quantidade disponível.

```python
itens_hotel = []

def adicionar_item(nome, preco, quantidade):
    itens_hotel.append({"nome": nome, "preco": preco, "quantidade": quantidade})

def remover_item(nome):
    for item in itens_hotel:
        if item["nome"] == nome:
            itens_hotel.remove(item)
            break

def listar_itens():
    print("Itens do hotel:")
    for item in itens_hotel:
        print("- Nome:", item["nome"], "| Preço:", item["preco"], "| Quantidade:", item["quantidade"])

adicionar_item("Toalha", 10, 20)
adicionar_item("Sabonete", 5, 30)
listar_itens()
```

#### Exemplo Avançado:

Vamos utilizar uma função lambda para ordenar os itens por preço antes de listar.

```python
itens_hotel = []

def adicionar_item(nome, preco, quantidade):
    itens_hotel.append({"nome": nome, "preco": preco, "quantidade": quantidade})

def remover_item(nome):
    for item in itens_hotel:
        if item["nome"] == nome:
            itens_hotel.remove(item)
            break

def listar_itens():
    print("Itens do hotel (ordenados por preço):")
    itens_ordenados = sorted(itens_hotel, key=lambda x: x["preco"])
    for item in itens_ordenados:
        print("- Nome:", item["nome"], "| Preço:", item["preco"], "| Quantidade:", item["quantidade"])

adicionar_item("Toalha", 10, 20)
adicionar_item("Sabonete", 5, 30)
adicionar_item("Shampoo", 15, 15)
listar_itens()
```

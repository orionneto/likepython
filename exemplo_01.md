Exemplo de um sistema de gestão de reservas em um hotel usando Python. Neste sistema, vamos implementar funcionalidades como adicionar novas reservas, verificar a disponibilidade de quartos, exibir informações sobre as reservas existentes e calcular o total de receita gerada. Vamos começar definindo algumas funcionalidades básicas:

1. Adicionar novas reservas.
2. Verificar a disponibilidade de quartos.
3. Exibir informações sobre as reservas existentes.
4. Calcular o total de receita gerada.

Vamos começar com a definição dos quartos do hotel e criar funções para realizar essas operações:

```python
# Definição dos quartos do hotel
quartos = {
    '101': {'tipo': 'simples', 'preco': 100},
    '102': {'tipo': 'duplo', 'preco': 150},
    '103': {'tipo': 'luxo', 'preco': 200}
}

# Lista de reservas
reservas = []

# Função para adicionar nova reserva
def adicionar_reserva(quarto, nome, dias):
    reservas.append({'quarto': quarto, 'nome': nome, 'dias': dias})

# Função para verificar disponibilidade de quartos
def verificar_disponibilidade(quarto, dias):
    if quarto in reservas:
        print(f"Quarto {quarto} está reservado.")
    else:
        print(f"Quarto {quarto} está disponível para reserva.")

# Função para exibir informações sobre as reservas
def exibir_reservas():
    for reserva in reservas:
        print(f"Quarto: {reserva['quarto']}, Nome: {reserva['nome']}, Dias: {reserva['dias']}")

# Função para calcular o total de receita gerada
def calcular_receita():
    total = 0
    for reserva in reservas:
        quarto = reserva['quarto']
        total += quartos[quarto]['preco'] * reserva['dias']
    return total

# Exemplo de uso das funções
adicionar_reserva('101', 'João', 3)
adicionar_reserva('103', 'Maria', 5)
verificar_disponibilidade('101', 3)
exibir_reservas()
print("Total de receita gerada:", calcular_receita())
```

Neste exemplo, usamos dicionários para representar os quartos do hotel e as reservas. As chaves dos dicionários são os números dos quartos. Cada quarto possui um tipo e um preço associado. As reservas são armazenadas em uma lista de dicionários, onde cada dicionário representa uma reserva com as informações do quarto, nome do cliente e número de dias da reserva.

Utilizamos funções para realizar diferentes operações, como adicionar uma nova reserva, verificar a disponibilidade de um quarto, exibir informações sobre as reservas existentes e calcular o total de receita gerada.

Este exemplo demonstra como combinar estruturas de controle como `if`, `while` e `for` com listas, dicionários e funções para criar um sistema simples de gestão de reservas em um hotel.

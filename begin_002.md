
### Lista:
- **Explicação simples**: Uma lista em Python é uma coleção ordenada e mutável de itens.
- **Exemplo simples**: 
  ```python
  lista_quartos = [101, 102, 103, 104]
  ```
- **Exemplo intermediário** (adicionando um novo quarto):
  ```python
  lista_quartos.append(105)
  ```
- **Exemplo avançado** (removendo um quarto):
  ```python
  lista_quartos.remove(102)
  ```

### Tupla:
- **Explicação simples**: Uma tupla em Python é uma coleção ordenada e imutável de itens.
- **Exemplo simples**:
  ```python
  dados_quarto = (101, 'Solteiro', 1, True)
  ```
- **Exemplo intermediário**: 
  Não é possível adicionar ou remover itens de uma tupla, mas você pode converter uma lista em tupla ou vice-versa.
- **Exemplo avançado**: 
  ```python
  # Convertendo lista para tupla
  lista_quartos = [101, 102, 103]
  tupla_quartos = tuple(lista_quartos)
  ```

### Pilha:
- **Explicação simples**: Uma pilha em Python é uma estrutura de dados onde o último elemento adicionado é o primeiro a ser removido (LIFO - Last In, First Out).
- **Exemplo simples**:
  ```python
  pilha_quartos = []
  pilha_quartos.append(101)  # Adiciona um quarto
  pilha_quartos.append(102)  # Adiciona outro quarto
  quarto_removido = pilha_quartos.pop()  # Remove o último quarto adicionado
  ```
- **Exemplo intermediário**: Implementação de uma classe de Pilha.
- **Exemplo avançado**: Utilização de uma pilha para gerenciar pedidos de reservas de quartos.

### Array:
- **Explicação simples**: Em Python, um array é semelhante a uma lista, mas é uma estrutura de dados homogênea, ou seja, todos os elementos devem ser do mesmo tipo.
- **Exemplo simples**: 
  ```python
  from array import array
  precos_quartos = array('f', [100.0, 120.5, 150.75])
  ```
- **Exemplo intermediário**: Operações aritméticas com arrays.
- **Exemplo avançado**: Utilização de um array para armazenar dados de vendas de quartos.

### Dicionário:
- **Explicação simples**: Um dicionário em Python é uma coleção de pares chave-valor, onde cada chave única mapeia para um valor.
- **Exemplo simples**: 
  ```python
  dados_quarto = {'numero': 101, 'tipo': 'Solteiro', 'andar': 1, 'disponivel': True}
  ```
- **Exemplo intermediário**: Acessando e modificando valores no dicionário.
- **Exemplo avançado**: Utilização de dicionários para armazenar informações de todos os quartos do hotel, com o número do quarto como chave e os detalhes como valores.

Essas estruturas de dados podem ser úteis para diversas tarefas de gerenciamento de dados em um sistema de cadastro de um hotel. Dependendo da complexidade do sistema, você pode escolher a estrutura de dados mais adequada para cada caso de uso.

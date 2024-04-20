## Exercícios de Python para Instrumentalização de Equipamentos Eletrônicos - Exemplos

---

Uma das práticas mais eficazes para aprender programação é a copiar e anotar códigos enquanto se estuda. Portanto, recomendamos que você utilize uma folha para realizar a cópia e anotações dos códigos apresentados durante o curso. Esse processo permite não apenas a memorização, mas também a compreensão profunda da lógica por trás de cada exemplo.

Além disso, encorajamos você a modificar os exemplos fornecidos e a escrever seu próprio código. Essa prática não apenas consolida seu entendimento dos conceitos apresentados, mas também desenvolve suas habilidades de resolução de problemas e criatividade na programação.

Lembre-se de revisar e refletir sobre o código escrito, buscando compreender não apenas o "como", mas também o "porquê" de cada instrução.

--- 

**1. Verificação de Tensão**

```python
def verificar_tensao(tensao):
  """
  Verifica se a tensão está dentro da faixa normal de operação.

  Argumentos:
    tensao (float): Valor da tensão lida pelo sensor.

  Retorna:
    str: Mensagem indicando se a tensão está normal ou fora da faixa.
  """
  if tensao >= 12 and tensao <= 15:
    mensagem = "Tensão normal!"
  else:
    mensagem = "Tensão fora da faixa! Alarme ativado."
  return mensagem

tensao_lida = 13.5  # Simula leitura de tensão

resultado_verificacao = verificar_tensao(tensao_lida)
print(resultado_verificacao)
```

**Explicação:**

* A função `verificar_tensao` recebe como parâmetro a tensão lida pelo sensor.
* Um `if` é utilizado para verificar se a tensão está dentro da faixa normal de operação (entre 12 e 15 volts).
* Se a tensão estiver dentro da faixa, a mensagem "Tensão normal!" é retornada.
* Se a tensão estiver fora da faixa, a mensagem "Tensão fora da faixa! Alarme ativado." é retornada.
* A variável `tensao_lida` simula o valor da tensão lida pelo sensor.
* A função `verificar_tensao` é chamada com o valor da tensão lida como argumento.
* O resultado da verificação é armazenado na variável `resultado_verificacao`.
* O resultado da verificação é impresso na tela.

**2. Controle de Temperatura**

```python
def controlar_temperatura(temperatura):
  """
  Controla a temperatura do sistema acionando ventilador ou aquecedor.

  Argumentos:
    temperatura (float): Valor da temperatura lida pelo sensor.
  """
  ventilador_ligado = False
  aquecedor_ligado = False

  if temperatura > 35:
    ventilador_ligado = True
    print("Ventilador ligado para resfriar o sistema.")
  elif temperatura < 20:
    aquecedor_ligado = True
    print("Aquecedor ligado para aquecer o sistema.")
  else:
    print("Temperatura dentro da faixa normal.")

  if ventilador_ligado:
    # Simular acionamento do ventilador
    pass
  if aquecedor_ligado:
    # Simular acionamento do aquecedor
    pass

temperatura_lida = 32  # Simula leitura de temperatura

controlar_temperatura(temperatura_lida)
```

**Explicação:**

* A função `controlar_temperatura` recebe como parâmetro a temperatura lida pelo sensor.
* As variáveis `ventilador_ligado` e `aquecedor_ligado` são inicializadas como `False`.
* Um `if` é utilizado para verificar se a temperatura está acima do limite superior (35 graus Celsius).
    * Se a temperatura estiver acima do limite, o ventilador é ligado e uma mensagem é impressa na tela.
    * A função `ventilador_ligado` é definida para `True` para simular o acionamento do ventilador.
* Um `elif` é utilizado para verificar se a temperatura está abaixo do limite inferior (20 graus Celsius).
    * Se a temperatura estiver abaixo do limite, o aquecedor é ligado e uma mensagem é impressa na tela.
    * A função `aquecedor_ligado` é definida para `True` para simular o acionamento do aquecedor.
* Um `else` é utilizado para indicar que a temperatura está dentro da faixa normal.
* As funções `ventilador_ligado` e `aquecedor_ligado` contêm comentários para indicar que a simulação do acionamento dos dispositivos seria implementada nestas funções.
* A variável `temperatura_lida` simula o valor da temperatura lida pelo sensor.
* A função `controlar_temperatura` é chamada com o valor da temperatura lida como argumento.

**3. Aquisição de Dados**

```python
def adquirir_dados():
  """
  Aquire dados de um sensor a cada segundo e calcula a média e o desvio padrão.
  """
  dados = []  # Lista para armazenar os dados

  for i in range(10):  # Simula 10 leituras a cada segundo
    valor_lido = random.uniform(10, 20



**Exemplo 4: Uso de Lista**

```python
def registrar_leituras(sensor, leituras):
    """
    Registra as leituras de um sensor em uma lista.

    Argumentos:
        sensor (str): Nome do sensor.
        leituras (list): Lista contendo as leituras do sensor.

    Retorna:
        list: Lista atualizada com as leituras do sensor.
    """
    print(f"Registrando leituras do sensor {sensor}:")
    for leitura in leituras:
        print(f"Leitura do sensor {sensor}: {leitura}")
    return leituras

leituras_sensor1 = [23.5, 24.0, 23.8, 24.2, 23.9]  # Lista de leituras do sensor 1
leituras_sensor2 = [18.7, 19.2, 18.5, 19.0, 18.9]  # Lista de leituras do sensor 2

leituras_sensor1 = registrar_leituras("Sensor 1", leituras_sensor1)
leituras_sensor2 = registrar_leituras("Sensor 2", leituras_sensor2)
```

**Explicação:**

- A função `registrar_leituras` recebe o nome de um sensor e uma lista de leituras desse sensor.
- Itera sobre as leituras e imprime cada uma delas, juntamente com o nome do sensor.
- Retorna a lista de leituras atualizada.
- As listas `leituras_sensor1` e `leituras_sensor2` representam as leituras de dois sensores diferentes.
- As leituras de cada sensor são registradas chamando a função `registrar_leituras` com o nome do sensor e a lista de leituras como argumentos.

Agora, vamos para o exemplo 5: Dicionário.

**5: Dicionário**

```python
def gerar_relatorio(sensor, leituras):
    """
    Gera um relatório com as leituras de um sensor.

    Argumentos:
        sensor (str): Nome do sensor.
        leituras (dict): Dicionário contendo as leituras do sensor.

    Retorna:
        str: Relatório com as leituras do sensor.
    """
    relatorio = f"Relatório de leituras do sensor {sensor}:\n"
    for chave, valor in leituras.items():
        relatorio += f"{chave}: {valor}\n"
    return relatorio

leituras_sensor1 = {"09:00": 23.5, "10:00": 24.0, "11:00": 23.8, "12:00": 24.2, "13:00": 23.9}  # Dicionário de leituras do sensor 1
leituras_sensor2 = {"09:00": 18.7, "10:00": 19.2, "11:00": 18.5, "12:00": 19.0, "13:00": 18.9}  # Dicionário de leituras do sensor 2

relatorio_sensor1 = gerar_relatorio("Sensor 1", leituras_sensor1)
relatorio_sensor2 = gerar_relatorio("Sensor 2", leituras_sensor2)

print(relatorio_sensor1)
print(relatorio_sensor2)
```

**Explicação:**

- A função `gerar_relatorio` recebe o nome de um sensor e um dicionário de leituras desse sensor, onde as chaves são os horários e os valores são as leituras.
- Itera sobre as chaves e valores do dicionário e constrói uma string de relatório.
- Retorna o relatório gerado.
- Os dicionários `leituras_sensor1` e `leituras_sensor2` representam as leituras de dois sensores diferentes, onde as chaves são os horários e os valores são as leituras.
- Um relatório para cada sensor é gerado chamando a função `gerar_relatorio` com o nome do sensor e o dicionário de leituras como argumentos.

Agora, continuaremos com o exemplo 6: Uso de Funções.

**6: Uso de Funções**

```python
def calcular_resistencia(volt, corrente):
    """
    Calcula a resistência de um componente eletrônico.

    Argumentos:
        volt (float): Tensão aplicada ao componente (em volts).
        corrente (float): Corrente que atravessa o componente (em ampères).

    Retorna:
        float: Valor da resistência (em ohms).
    """
    resistencia = volt / corrente
    return resistencia

# Valores de tensão e corrente medidos
tensao = 12.5  # Volts
corrente = 0.5  # Ampères

resistencia = calcular_resistencia(tensao, corrente)
print(f"A resistência do componente é de {resistencia} ohms.")
```

**Explicação:**

- A função `calcular_resistencia` recebe a tensão aplicada a um componente e a corrente que atravessa o componente.
- Calcula a resistência do componente usando a fórmula de Ohm (resistência = tensão / corrente).
- Retorna o valor da resistência calculada.
- Os valores de tensão e corrente medidos são utilizados para calcular a resistência do componente chamando a função `calcular_resistencia`.

Agora, vamos para o exemplo 7: Uso de Funções com Argumento.

**7: Uso de Funções com Argumento**

```python
def verificar_corrente(corrente, limite):
    """
    Verifica se a corrente está dentro do limite especificado.

    Argumentos:
        corrente (float): Corrente medida (em ampères).
        limite (float): Limite máximo de corrente permitido (em ampères).

    Retorna:
        str: Mensagem indicando se a corrente está dentro do limite ou não.
    """
    if corrente <= limite:
        return f"Corrente dentro do limite de {limite} ampères."
    else:
        return f"Corrente excedeu o limite de {limite} ampères. Verificar sistema."

# Valor da corrente medida
corrente_medida = 0.6  # Ampères
limite_corrente = 0.5  # Ampères

mensagem_verificacao = verificar_corrente(corrente_medida, limite_corrente)
print(mensagem_verificacao)
```

**Explicação:**

- A função `verificar_corrente` recebe a corrente medida e um limite máximo de corrente permitido.
- Verifica se a

 corrente medida está dentro do limite especificado.
- Retorna uma mensagem indicando se a corrente está dentro do limite ou se excedeu o limite.
- O valor da corrente medida e o limite máximo de corrente permitido são utilizados para verificar se a corrente está dentro do limite chamando a função `verificar_corrente`.

Agora, o exemplo 8: Uso Lista + Uso do If e Else.

**8: Uso Lista + Uso do If e Else**

```python
def verificar_sensores(sensores):
    """
    Verifica o estado de funcionamento dos sensores.

    Argumentos:
        sensores (list): Lista contendo o estado de cada sensor (True para funcionando, False para não funcionando).

    Retorna:
        str: Mensagem indicando o estado de funcionamento de cada sensor.
    """
    for i, sensor in enumerate(sensores):
        if sensor:
            print(f"Sensor {i+1}: Funcionando normalmente.")
        else:
            print(f"Sensor {i+1}: Com mau funcionamento. Verificar.")

# Estado de funcionamento dos sensores (True para funcionando, False para não funcionando)
sensores_estado = [True, False, True, True]

verificar_sensores(sensores_estado)
```

**Explicação:**

- A função `verificar_sensores` recebe uma lista contendo o estado de funcionamento de cada sensor.
- Itera sobre a lista de sensores e verifica o estado de cada um.
- Se o sensor estiver funcionando (valor True), imprime que está funcionando normalmente. Caso contrário, imprime que está com mau funcionamento.
- A lista `sensores_estado` representa o estado de funcionamento de cada sensor.
- O estado de funcionamento de cada sensor é verificado chamando a função `verificar_sensores`.

Agora, o exemplo 9: Uso de Operadores Lógicos.

**9: Uso de Operadores Lógicos**

```python
def verificar_circuitos(circuito1, circuito2):
    """
    Verifica se os circuitos estão ambos fechados.

    Argumentos:
        circuito1 (bool): Estado do circuito 1 (True para fechado, False para aberto).
        circuito2 (bool): Estado do circuito 2 (True para fechado, False para aberto).

    Retorna:
        str: Mensagem indicando se ambos os circuitos estão fechados ou não.
    """
    if circuito1 and circuito2:
        return "Ambos os circuitos estão fechados."
    else:
        return "Pelo menos um dos circuitos está aberto. Verificar."

# Estados dos circuitos (True para fechado, False para aberto)
circuito1_estado = True
circuito2_estado = False

mensagem_verificacao = verificar_circuitos(circuito1_estado, circuito2_estado)
print(mensagem_verificacao)
```

**Explicação:**

- A função `verificar_circuitos` recebe o estado de dois circuitos.
- Utiliza o operador lógico "and" para verificar se ambos os circuitos estão fechados.
- Retorna uma mensagem indicando se ambos os circuitos estão fechados ou se pelo menos um deles está aberto.
- Os estados dos circuitos são representados por valores booleanos (True para fechado e False para aberto).
- O estado dos circuitos é verificado chamando a função `verificar_circuitos`.

Por fim, o exemplo 10: Uso While + Uso de Laço For, + Uso de Lista + Uso de Operadores Lógicos.

**Exemplo 10: Uso While + Uso de Laço For, + Uso de Lista + Uso de Operadores Lógicos**

```python
def verificar_leituras(leituras):
    """
    Verifica se todas as leituras estão dentro da faixa normal.

    Argumentos:
        leituras (list): Lista contendo as leituras a serem verificadas.

    Retorna:
        str: Mensagem indicando se todas as leituras estão dentro da faixa normal ou não.
    """
    faixa_normal = range(10, 20)  # Faixa normal de leituras
    for leitura in leituras:
        if leitura not in faixa_normal:
            return "Pelo menos uma leitura está fora da faixa normal. Verificar."
    return "Todas as leituras estão dentro da faixa normal."

# Simulação de leituras
leituras = [12, 15, 17, 19, 14, 13, 16, 18, 21, 20]
mensagem_verificacao = verificar_leituras(leituras)
print(mensagem_verificacao)
```

**Explicação:**

- A função `verificar_leituras` recebe uma lista de leituras a serem verificadas.
- Define a faixa normal de leituras como valores entre 10 e 19.
- Utiliza um laço `for` para iterar sobre cada leitura na lista.
- Verifica se cada leitura está dentro da faixa normal utilizando o operador `not in`.
- Retorna uma mensagem indicando se todas as leituras estão dentro da faixa normal ou se pelo menos uma delas está fora.
- Uma lista de leituras é simulada e passada para a função `verificar_leituras` para verificação.

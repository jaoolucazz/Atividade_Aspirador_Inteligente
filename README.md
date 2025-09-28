# - Perceptron Aspirador Inteligente

## Descrição

Este repositório contém a implementação de um modelo de perceptron simples para controlar um **aspirador inteligente**. O objetivo do projeto é ajustar dois parâmetros importantes — **potência** e **velocidade** — do aspirador com base nas condições de operação, como o tipo de piso, o nível de sujeira e a distância percorrida.

## Objetivo

O perceptron foi desenvolvido para simular o comportamento de um aspirador inteligente que se adapta dinamicamente ao ambiente. O modelo calcula a potência e a velocidade do aspirador em função de três entradas principais:

* **Piso**: Tipo de superfície em que o aspirador está operando (exemplo: madeira, cerâmica, carpete).
* **Sujeira**: Nível de sujeira presente na superfície.
* **Distância**: Distância percorrida pelo aspirador.

## Resolução do Problema

A lógica do modelo é baseada na análise dos seguintes fatores:

1. **Potência**: O cálculo da potência é proporcional ao nível de sujeira. Quanto maior o valor de sujeira, maior será a potência necessária para realizar a limpeza.
2. **Velocidade**: A velocidade é ajustada levando em consideração o tipo de piso e a distância percorrida. O piso mais difícil de limpar (como carpete) exige uma velocidade menor, enquanto pisos mais fáceis (como cerâmica) permitem uma velocidade maior.

A potência é ajustada em um intervalo determinado, enquanto a velocidade é limitada entre 1 e 5 para garantir que o aspirador opere de forma eficiente.

## Procedimento de Execução

### Requisitos

* Python 3.x
* Nenhuma biblioteca externa necessária.

### Como executar

1. Clone o repositório para o seu computador:

   ```bash
   git clone https://github.com/seuusuario/perceptron-aspirador-inteligente.git
   ```

2. Navegue até a pasta do projeto:

   ```bash
   cd perceptron-aspirador-inteligente
   ```

3. Execute o código no Python:

   ```bash
   python perceptron_aspirador.py
   ```

### Função `perceptron_aspirador_inteligente`

A função `perceptron_aspirador_inteligente` é responsável por calcular a potência e a velocidade com base nas entradas fornecidas. A assinatura da função é a seguinte:

```python
def perceptron_aspirador_inteligente(piso, sujeira, distancia):
```

**Parâmetros**:

* `piso`: Tipo de piso (string: "madeira", "ceramica", "carpete").
* `sujeira`: Nível de sujeira (número inteiro, de 0 a 10).
* `distancia`: Distância percorrida pelo aspirador (número inteiro).

**Retorno**:
A função retorna dois valores:

* `potencia`: A potência ajustada do aspirador.
* `velocidade`: A velocidade ajustada do aspirador.

### Exemplos de Execução

Aqui estão alguns exemplos de uso da função:

```python
print(perceptron_aspirador_inteligente("madeira", 6, 4))  
# Saída: (potência ajustada, velocidade ajustada)

print(perceptron_aspirador_inteligente("ceramica", 10, 2))
# Saída: (potência ajustada, velocidade ajustada)

print(perceptron_aspirador_inteligente("carpete", 3, 1))
# Saída: (potência ajustada, velocidade ajustada)
```

### Exemplo de Saída

```bash
(2, 3)
(3, 3)
(1, 2)
```

## Conclusão

Este projeto fornece uma base para o controle inteligente de um aspirador, ajustando sua potência e velocidade com base nas condições do ambiente. O código pode ser expandido e melhorado para incluir mais parâmetros de ajuste, como um sensor de sujeira, ou até ser integrado a um sistema real de controle de dispositivos.

# Métodos de Resolução de Problemas em IA - Atividade Laboral

Este repositório contém a implementação de algoritmos de busca e resolução de problemas aplicados à Inteligência Artificial. O foco atual é a implementação do algoritmo de busca **A* (A-Estrela)** para navegação em grades bidimensionais com obstáculos.

## 🚀 Sobre o Projeto

O objetivo deste código é encontrar o caminho mais curto entre um ponto inicial e um ponto de destino em uma matriz (grade), desviando de obstáculos. O algoritmo utiliza a **Distância de Manhattan** como função heurística, sendo ideal para movimentos em quatro direções (cima, baixo, esquerda, direita).

### 🧠 O Algoritmo A*

O algoritmo funciona minimizando a função:


$$f(n) = g(n) + h(n)$$

Onde:

* **$g(n)$**: É o custo real do caminho do nó inicial até o nó atual $n$.
* **$h(n)$**: É o custo estimado (heurística) do nó $n$ até o objetivo.

No caso desta implementação, como o movimento é em grade com custo unitário, $g(n)$ aumenta em 1 para cada passo e $h(n)$ é calculado pela distância entre as coordenadas $(x, y)$.

---

## 🛠️ Funcionalidades

* **Busca A* customizada**: Implementação eficiente utilizando `heapq` (fila de prioridade).
* **Detecção de Obstáculos**: O algoritmo ignora células bloqueadas (valor `1`).
* **Visualização no Terminal**: Função para imprimir a grade mostrando o caminho percorrido (`*`), obstáculos (`#`) e espaços vazios (`.`).
* **Heurística de Manhattan**: Otimizada para grades retangulares.

---

## 💻 Como Executar

### Pré-requisitos

* Python 3.x instalado.

### Passo a Passo

1. Clone o repositório:
```bash
git clone https://github.com/rafael-calixto1/Metodos-De-Resolucao-De-Problemas-Em-IA.git

```


2. Navegue até o diretório:
```bash
cd Metodos-De-Resolucao-De-Problemas-Em-IA

```


3. Execute o script principal:
```bash
python nome_do_seu_arquivo.py

```



---

## 📊 Exemplo de Saída

Ao executar o código, você verá uma representação visual do caminho encontrado:

```text
Caminho encontrado com custo 18 (número de passos).
Caminho: [(0, 0), (0, 1), (0, 2), ...]

* * * * * . . . . .
. # # # * . # # # .
. . . # * * * * # .
# # . # . # # * # .
. . . . . . # * * *
. # # # # . # # # *
. . . . # . . . . *
# # . . # . # # # *
. . . . . . . . # *
. # # # # # # . . *

```

---

## 📁 Estrutura do Código

* `astar_grade`: Função principal que executa a lógica de busca.
* `manhattan`: Calcula a distância estimada até o alvo.
* `vizinhos`: Mapeia os movimentos possíveis dentro dos limites da grade.
* `imprime_grade_com_caminho`: Renderiza a grade formatada para leitura humana.

---


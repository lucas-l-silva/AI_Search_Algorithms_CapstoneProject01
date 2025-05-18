# Projeto 01 – Inteligência Artificial  
**Curso de Ciência de Dados – Universidade Federal do Ceará (UFC)**  
Disciplina: Inteligência Artificial – 2025.1  

## 🎯 Descrição Geral

Este projeto abrange dois tópicos fundamentais da disciplina:

1. **Algoritmos de Busca em Grafos Ponderados**
   - Implementação dos algoritmos:  
     - BFS (Busca em Largura)  
     - UCS (Busca de Custo Uniforme)  
     - Greedy (Busca Gulosa com heurística admissível)  
     - A\* (Busca A Estrela com heurística admissível)  
   - Avaliação de custo, nós expandidos e tempo de execução
   - Validação e visualização da heurística
   - Comparação entre algoritmos com gráficos horizontais

2. **Otimização Local com Hill Climbing**
   - Minimização da função não convexa:  
     \[
     f(x, y) = x^2 + y^2 + 25(\sin^2 x + \sin^2 y)
     \]
   - Versão simples (sem reinício)
   - Versão com reinício aleatório (10 execuções)
   - Visualização 3D com trajetórias e análise gráfica

---

## 📁 Estrutura do Repositório

```bash
projeto01/
├── projeto01.ipynb               # Notebook com implementação completa e resultados
├── relatorio_projeto01.tex      # Relatório técnico (LaTeX)
├── projeto01_apresentacao.tex   # Slides em LaTeX com Beamer
├── figuras/                     # Imagens geradas (grafo, heurística, trajetórias)
│   ├── Grafo.png
│   ├── Heuristica.png
│   ├── Caminho Busca A_star.png
│   ├── Caminho Busca Gulosa.png
│   ├── Caminho Busca em Largura.png
│   ├── Caminho Busca de Custo Uniforme.png
│   ├── Trajetória do Hill Climbing.png
│   ├── Trajetórias do Hill Climbing com Reinício Aleatório.png
│   └── Comparação de Desempenho entre Algoritmos de Busca.png
---
```

## 📊 Resultados – Busca em Grafos

| Algoritmo | Caminho    | Custo | Expansões | Tempo (ms) |
|-----------|------------|-------|-----------|-------------|
| BFS       | A → H → G  | 13    | 7         | 1.085       |
| UCS       | A → B → G  | **9** | 6         | 0.088       |
| Greedy    | A → C → G  | 14    | 3         | 0.052       |
| A*        | A → B → G  | **9** | 6         | 0.057       |

- A heurística foi validada por admissibilidade usando UCS.
- O algoritmo A* obteve o melhor equilíbrio entre custo e eficiência.

---

## 📉 Resultados – Hill Climbing

- A versão básica ficou presa em mínimo local: $f = 47.42$  
- O melhor reinício aleatório obteve: $f = 9.5474$  
- Nenhuma execução atingiu o mínimo global $f(0,0) = 0$, mas houve boa aproximação

Visualizações 3D das trajetórias foram utilizadas para análise visual da eficiência e convergência.

---

## 📄 Relatório e Apresentação

📘 Relatório acadêmico em LaTeX:  
[→ Visualizar PDF no Overleaf](https://www.overleaf.com/read/bwphwmbczxkh#9a13e5)

📽️ Slides da apresentação final (Beamer):  
[→ Visualizar apresentação](https://www.overleaf.com/read/bwphwmbczxkh#9a13e5)

---

## 👥 Integrantes

- Lucas Lopes Silva
- Artur Saraiva Paschoal
- Artur Garcia Sales Barroso

---

## 🛠️ Tecnologias

- Python 3.10  
- Bibliotecas: `networkx`, `matplotlib`, `plotly`, `numpy`, `heapq`, `time`
- LaTeX (Overleaf e Beamer)

---

## 📌 Como executar

Execute o notebook `projeto01.ipynb` célula a célula em um ambiente com Jupyter, ou visualize os resultados no PDF do relatório.

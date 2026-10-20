# Trabalho de Computação Escalável - Grupo 6

Repositório dedicado ao desenvolvimento do Trabalho Prático da disciplina de **Computação Escalável** (2026/2).

## Integrantes
* **Guilherme Terziotti** ([@guiterzi](https://github.com/guiterzi))
* **Lucas Silva** ([@luticaa](https://github.com/luticaa))
* **Marcos Vinicius Beregula** ([@MarcosDataScientist](https://github.com/MarcosDataScientist))

---

## 📌 Escopo do Projeto (Grupo de 3 Pessoas)
* **Tarefa:** Agrupamento / Clustering
* **Algoritmo:** GMM (*Gaussian Mixture Models*)
* **Decomposições Avaliadas:**
  1. **Decomposição 1:** *(A definir, ex.: Particionamento de Dados no E-step via ExecutorService / ThreadPool)*
  2. **Decomposição 2:** *(A definir, ex.: Decomposição Recursiva divide-and-conquer via ForkJoinPool)*

Para a íntegra das regras e cronograma da disciplina, consulte [`instrucoes_trabalho.md`](./instrucoes_trabalho.md).

---

## ⚙️ Estrutura de Diretórios Sugerida

```text
trabalho/
├── instrucoes_trabalho.md       # Diretrizes oficiais e cronograma
├── README.md                    # Apresentação do projeto e manual de execução
├── datasets/                    # Datasets de teste (ou scripts geradores sintéticos)
│   ├── dataset_1/
│   └── dataset_2/
├── src/                         # Código-fonte
│   ├── common/                  # Interface comum e leitura de dados
│   ├── decomposicao1/           # Implementação Concorrente 1
│   └── decomposicao2/           # Implementação Concorrente 2
├── scripts/                     # Scripts de benchmark e plot dos gráficos
└── docs/                        # Relatório técnico e documentação
```

---

## 🚀 Como Compilar e Executar

*(Instruções a serem preenchidas conforme a implementação for desenvolvida)*

```bash
# Exemplo de compilação
javac -d bin src/**/*.java

# Exemplo de execução Decomposição 1
java -cp bin com.escalavel.Main --decomp 1 --dataset datasets/dataset_1.csv

# Exemplo de execução Decomposição 2
java -cp bin com.escalavel.Main --decomp 2 --dataset datasets/dataset_1.csv
```

---

## 🤖 Declaração de Uso de Inteligência Artificial

Em conformidade com as regras estabelecidas pela Profa. Larissa (Slide 38):
* **Lógica Concorrente dos Algoritmos:** Desenvolvida integralmente pelos integrantes, sem auxílio de IA.
* **Leitura/Parsing de Arquivos:** *(Especificar se foi utilizada e em quais arquivos)*
* **Scripts de Benchmark / Gráficos:** *(Especificar se foi utilizada e em quais arquivos)*

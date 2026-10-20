# Trabalho Prático de Computação Escalável (2026/2)

Este documento centraliza todas as instruções oficiais, requisitos específicos, cronograma e definições do trabalho semestral da disciplina de **Computação Escalável** (Profa. Larissa).

---

## 1. Identificação do Grupo

* **Grupo:** Grupo 6 (*Único grupo com 3 integrantes da turma*)
* **Integrantes:**
  * **Guilherme Terziotti**
  * **Lucas Silva**
  * **Marcos Vinicius Beregula**
* **Status no Classroom:** Fechado (registrado na planilha oficial da turma em 12/10/2026)
* **Tarefa Escolhida:** Agrupamento / Clustering
* **Algoritmo / Proposta:** GMM (*Gaussian Mixture Models*) / PCA
* **Planilha Oficial:** [Planilha de Organização dos Grupos](https://docs.google.com/spreadsheets/d/1LHmx90xq5qtyfymDBIdLKNk3OIvnywu50Y1za-kMxKg/edit?usp=drive_web)

---

## 2. Requisitos Específicos para o Grupo de 3 Integrantes

Conforme apresentado em sala e documentado no material oficial (**Slide 35** da Aula 08 / 09):

* **Escolha do Algoritmo:** Implementar **1 algoritmo** de Ciência de Dados (diferente dos grupos de 4 que precisam fazer 2 algoritmos).
* **Implementação Concorrente:** Implementar esse algoritmo aplicando **2 decomposições diferentes** de dados ou tarefas:
  * Exemplo: dois métodos distintos de particionamento de dados, divisão de domínio vs. pipeline mestre-trabalhador, particionamento estático em blocos vs. divisão recursiva com `ForkJoinPool`, etc.
* **Padronização:** Ambas as decomposições devem obrigatoriamente rodar sob a **mesma interface de execução** e gerar o **mesmo formato de saída (*output*)**, viabilizando uma comparação justa de desempenho e escalabilidade.

---

## 3. Diretrizes Técnicas e Tecnologias

* **Linguagem & Frameworks:**
  * **Java:** Utilizando primitivas e abstrações concorrentes vistas na disciplina (`Threads`, `ExecutorService` e `ForkJoinPool`).
  * **Scala:** Sobre o ecossistema **Apache Spark** (map-reduce distribuído).
  * *Regra:* Ambos os modelos/decomposições devem ser implementados na mesma linguagem.
* **Datasets para os Testes:**
  * **Quantidade:** Selecionar ou gerar **2 datasets distintos**.
  * **Origem:** Datasets reais (ex.: base do Cempre / Mineração de Dados do Prof. Menolli) ou sintéticos (com distribuições estatísticas diferentes).
  * **Volume:** De **10.000 a 150.000 pontos** (na escala de 100k registros).
* **Avaliação de Escalabilidade:**
  * Aumentar o volume de dados progressivamente (ex.: de 10k em 10k pontos) e cronometrar o tempo de execução.
  * **Importante:** Medir estritamente o tempo de processamento do algoritmo (desconsiderar leitura inicial de disco/I/O e inicialização de bibliotecas/framework).
  * **Gráficos:** Gerar 1 gráfico por dataset (Eixo X = Número de instâncias/dados, Eixo Y = Tempo de execução em ms/s) com 2 curvas comparando as 2 decomposições.

---

## 4. Política de Uso de Inteligência Artificial

* ❌ **Proibido:** Uso de IA para implementação da lógica central do algoritmo concorrente/distribuído.
*  **Permitido:** 
  1. Funções utilitárias de leitura inicial e parsing de arquivos.
  2. Scripts para automação dos testes de benchmark e geração dos gráficos (*plots* de escalabilidade).
* **Obrigatoriedade:** Constar de forma transparente no `README.md` e no Relatório Final se IA foi utilizada, especificando quais arquivos e para quais rotinas.

---

## 5. Cronograma Oficial de Prazos e Apresentação

| Data Limite | Marco | Descrição |
| :--- | :--- | :--- |
| **25/10/2026** | **Formulário Inicial (Google Forms)** | Cadastro oficial dos integrantes, tarefa, algoritmo, detalhamento das 2 decomposições e link do repositório GitHub. |
| **12/11/2026** | **Entrega do Relatório Final** | Submissão do relatório técnico (template será disponibilizado pela professora no Classroom). |
| **13/11/2026** | **Apresentação Final** | Apresentação de ~20 minutos por grupo em aula detalhando arquitetura, decisões de paralelismo e resultados. |
| **27/11/2026** | *Prova 2 (P2)* | Avaliação teórica da disciplina. |

---

## 6. Contexto da Discussão da Equipe (Alinhamento WhatsApp)

1. **Definição da Formação:**
   * Grupo fechado com 3 pessoas: Guilherme, Lucas e Marcos.
   * Vantagem competitiva: foco em 1 único algoritmo bem implementado e refinado sob 2 técnicas de decomposição, ao invés de codificar 2 algoritmos completos.
2. **Estratégia do Algoritmo e Dados:**
   * Reuso inteligente: aproveitar os datasets já manipulados na matéria de Mineração de Dados (Prof. Menolli) para ganhar velocidade.
   * Algoritmos simples como K-Means e DBSCAN foram reservados pelo Grupo 3.
   * O grupo reservou **GMM (*Gaussian Mixture Models*)** na planilha da turma (podendo integrar com PCA para redução dimensional ou explorar decomposições clássicas do algoritmo Expectation-Maximization).
3. **Plano de Execução Imediato:**
   * [ ] Definir as 2 estratégias de decomposição do GMM (ex.: Decomposição de Amostras/Dados no E-step vs. Paralelismo de Misturas/Clusters no M-step, ou `ExecutorService` vs. `ForkJoinPool`).
   * [ ] Criar o repositório no GitHub para o projeto.
   * [ ] Separar e preparar os 2 datasets (10k a 150k linhas).
   * [ ] Enviar o formulário inicial do Google Classroom até 25/10.

# AP1 - Análise de Dados do Restaurante Universitário (PRAE/UFC)

Este projeto apresenta a resolução da avaliação **AP1** da disciplina de **Laboratório de Ciência de Dados**. O objetivo principal é realizar uma análise exploratória e estatística sobre o consumo de refeições no Restaurante Universitário, utilizando dados reais fornecidos pela PRAE (Pró-Reitoria de Assuntos Estudantis).

## 📋 Informações do Aluno

* **Nome:** Cícero Rogério
* **Disciplina:** Laboratório de Ciência de Dados
* **Ferramenta:** Google Colab / Jupyter Notebook

## 🎯 Objetivos da Análise

O notebook aborda três questões principais para extrair *insights* sobre o comportamento dos comensais:

1. **Perfilamento de Consumo (Agregação):**
* Criação de "Perfis" combinando Vínculo (ex: Discente, Docente) + Categoria (Pagante/Isento) + Tipo de Refeição (Almoço/Jantar).
* Geração de estatísticas descritivas para cada perfil: Total de refeições, Média, Mediana, Desvio Padrão e Participação Percentual no total.


2. **Análise de Distribuição (Estatística):**
* Estudo da frequência de refeições por CPF único.
* Visualização através de **Histogramas** e verificação de normalidade dos dados utilizando o gráfico **Q-Q Plot** (Quantile-Quantile).


3. **Cálculo de Probabilidade (Interseção de Conjuntos):**
* Análise focada no grupo "Docentes".
* Cálculo da probabilidade de um docente que almoçou também ter jantado no RU (Interseção ).



## 🗂️ Sobre os Dados

* **Fonte:** `ap1-ufc-prae-comensais-2024.csv`
* **Descrição das Variáveis:**
* `cpf_cnpj`: Identificador anonimizado do usuário.
* `vinculo_comensal`: Tipo de usuário (Discente, Docente, Servidor, etc.).
* `categoria_acesso`: Status de pagamento (Pagante, Isento, etc.).
* `tipo_refeicao`: Refeição realizada (Almoço, Jantar, Café).
* `quantidade_refeicao`: Volume de refeições registradas.



## 🛠️ Tecnologias Utilizadas

O projeto foi desenvolvido em **Python 3** utilizando as seguintes bibliotecas:

* **Pandas:** Para manipulação, agregação e limpeza dos dados (`groupby`, `agg`).
* **Matplotlib & Seaborn:** Para visualização de dados (Histogramas).
* **Scipy (scipy.stats):** Para testes estatísticos e plotagem do gráfico de probabilidade normal (Probplot).

## 📊 Resultados em Destaque

* **Identificação de Perfis:** O código classifica e ordena os grupos que mais utilizam o restaurante (ex: *Discente + Pagante + Almoço*), permitindo entender a demanda principal.
* **Distribuição de Dados:** A análise visual (Histograma e Q-Q Plot) demonstra que a distribuição de refeições por CPF **não segue uma distribuição normal**, apresentando uma forte assimetria (muitos usuários com poucas refeições e poucos usuários "heavy users").
* **Probabilidade Condicional:** Foi calculado que aproximadamente **20%** dos docentes que almoçam no RU também retornam para o jantar.

## 🚀 Como Executar

1. Certifique-se de ter o Python instalado com as bibliotecas necessárias:
```bash
pip install pandas matplotlib seaborn scipy

```


2. Abra o arquivo `Cicero_Rogerio_LABCD.ipynb` no Jupyter Notebook, VS Code ou Google Colab.
3. Execute as células sequencialmente. O código baixará automaticamente o dataset do repositório remoto configurado na variável `arquivo`.

---

*Projeto acadêmico desenvolvido para fins avaliativos.*
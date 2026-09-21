# 🚢 Análise Exploratória de Dados do Titanic (Titanic EDA)

Projeto de análise exploratória de dados e engenharia de atributos (*Feature Engineering*) baseado no clássico desafio do Titanic. O objetivo desta etapa inicial foi realizar a limpeza, tradução e estruturação dos dados brutos para extrair insights valiosos e preparar o terreno para futuras etapas de Machine Learning.

---

## 📊 Informações Gerais do Dataset
* **Total de Linhas:** 891 registros
* **Total de Colunas:** 12 colunas (todas renomeadas para o português para facilitar a legibilidade)

---

## 🛠️ Tratamento e Limpeza de Dados
Durante a inspeção inicial, foram identificados valores nulos e tomadas decisões analíticas conscientes para preservar a integridade do conjunto de dados:

* **Idade (177 valores nulos):** Optou-se por **não alterar** ou preencher esses valores no momento, evitando o risco de introduzir viés estatístico ou distorcer análises futuras por faixa etária.
* **Cabine (687 valores nulos):** Foi feita uma investigação para tentar recuperar dados cruzando informações de bilhetes compartilhados. Foi possível recuperar apenas 1 valor pertencente ao bilhete `113781` (passageiros viajando em grupo onde apenas um estava sem a cabine preenchida). Os demais permaneceram como dados ausentes.
* **Porto de Embarque (2 valores nulos):** Analisado o contexto, sem encontrar padrões em comum para recuperação segura neste momento inicial.

---

## ⚙️ Engenharia de Atributos (*Feature Engineering*)
Para enriquecer a base de dados e facilitar futuras análises, as seguintes transformações e novas colunas foram criadas:

1. **Extração de Títulos:** Os títulos de nobreza e tratamento foram extraídos a partir dos nomes dos passageiros, categorizados em: `Mr`, `Miss`, `Mrs`, `Master` e agrupando os demais como `Outros`.
2. **Tamanho da Família:** Criação de uma coluna somando o total de membros familiares a bordo de cada passageiro.
3. **Mapeamento de Decks:** Extração da inicial da cabine para identificar a localização física no navio, resultando nas categorias: `C`, `B`, `D`, `E`, `A`, `F`, `G`, `T` e `Desconhecido`.
4. **Tradução das Classes:** A coluna de classe socioeconômica foi renomeada para facilitar a interpretação:
   * `1` ➔ Alta
   * `2` ➔ Média
   * `3` ➔ Baixa
5. **Faixas Etárias:** Criação de uma segmentação por idade para análises demográficas:
   * **Criança:** 0 a 12 anos
   * **Adolescente:** 12 a 18 anos
   * **Jovem:** 18 a 35 anos
   * **Adulto:** 35 a 60 anos
   * **Idoso:** 60 a 100 anos

---

## 🚀 Próximos Passos
Este repositório representa a primeira versão (MVP) do projeto. Nas próximas etapas, planejo implementar:
* Inclusão e detalhamento de gráficos e visualizações estatísticas da EDA.
* Tratamento final de variáveis categóricas (*One-Hot Encoding*).
* Construção e avaliação de modelos preditivos de Machine Learning.

---

## 👨‍💻 Autor
Desenvolvido por **Luiz Fernando de Jesus Silva Homem**.

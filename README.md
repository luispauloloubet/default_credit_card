# Análise de Risco de Crédito: Previsão de Inadimplência


Este repositório apresenta uma análise exploratória de dados (EDA) detalhada sobre uma base de dados de cartões de crédito (UCI), com o objetivo de identificar os principais preditores de inadimplência (*default*) e fornecer subsídios para modelos de *credit scoring*.

## Principais Insights da Análise

Diferente de suposições genéricas, a análise técnica revelou que os fatores financeiros superam significativamente os demográficos na previsão de risco:

1.  **Fatores Determinantes (Top 3):**
    * **Histórico de Atraso (PAY_X):** É o fator mais gritante. A probabilidade de inadimplência explode conforme o número de meses de atraso aumenta.
    * **Limite do Cartão (LIMIT_BAL):** Clientes com limites menores apresentam taxas de inadimplência muito mais altas. O banco tende a dar mais crédito a quem já provou ser bom pagador.
    * **Taxa de Utilização:** Quanto maior o uso do limite disponível, maior o risco de *default*.

2.  **Comportamento de Pagamento:**
    * **Taxa de Pagamento:** Clientes que pagam menos de 20% do valor da fatura de forma recorrente têm uma tendência altíssima à inadimplência.
    * **Histórico Tardio (FPD):** Clientes que já apresentavam atrasos há 6 meses (PAY_6) têm uma probabilidade **4x maior** de entrar em *default* no mês atual.

3.  **Variáveis Demográficas (Menos Significativas):**
    * **Idade:** Apresenta um comportamento parabólico (maior risco no início da vida financeira, estabiliza e volta a subir na maturidade).
    * **Escolaridade:** A inadimplência diminui conforme o nível de instrução aumenta.
    * **Sexo e Estado Civil:** Homens e casados apresentam um risco ligeiramente superior, mas a variação é pequena (~5%) comparada aos fatores financeiros.

## Tecnologias Utilizadas

* **Linguagem:** Python
* **Análise de Dados:** `Pandas`, `NumPy`
* **Visualização:** `Matplotlib`, `Seaborn` (com estilos personalizados)
* **Plataforma:** Google Colab

## Conclusão do Estudo

O estudo conclui que o **histórico financeiro e o comportamento de uso do crédito** são os verdadeiros pilares para a análise de risco. Variáveis demográficas, embora relevantes, não devem ser o foco principal de um modelo de concessão de crédito de alta precisão.


**Autor:** Luis Paulo Loubet  

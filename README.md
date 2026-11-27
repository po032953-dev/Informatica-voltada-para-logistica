# Informática-aplicada-a-logística
Trabalho de informática - Apresentação em equipe
<img width="233" height="438" alt="image" src="https://github.com/user-attachments/assets/c16569cf-0d20-480a-a307-073965c107e9" />



Esta é uma atividade em grupo, que, fiz junto do João Pedro e Hemilly Christine. Falamos um pouco sobre aquilo que nós gostamos e algumas experiências pessoais.


# Gráficos com dados abertos da ANTT
<img width="1182" height="861" alt="image" src="https://github.com/user-attachments/assets/46cf2fe6-8cfb-428c-a0f3-96667ee76f28" />


Durante esta atividade, tive a oportunidade de trabalhar com uma base de dados disponibilizada pela ANTT e utilizar o Excel para organizar e analisar as informações. Ao longo do processo, desenvolvi tabelas, gráficos e algumas análises que ajudaram a visualizar melhor os dados e identificar informações importantes presentes na planilha.

A realização dessa atividade também contribuiu para meu aprendizado sobre tratamento e interpretação de dados, mostrando na prática como uma grande quantidade de informações pode ser organizada de maneira mais clara. Além disso, o uso dos gráficos facilitou a compreensão dos resultados e tornou a apresentação das informações mais objetiva.

Esse trabalho serviu como uma experiência inicial na área de análise de dados e ajudou a desenvolver conhecimentos que poderão ser utilizados nas próximas atividades, principalmente na criação de análises mais completas e na utilização de ferramentas como o Power BI.

# Gráficos e perguntas com os dados abertos de São Paulo

<img width="1305" height="598" alt="image" src="https://github.com/user-attachments/assets/814be2ce-b102-489d-b40f-dedb7d97da90" />

Nesta atividade, foram analisados dados dos municípios do estado de são paulo para criar perguntas e comparações que podem ser reproduzidas no power bi. a proposta foi organizar as informações em diferentes análises, utilizando quantidade de municípios, regiões, drs e área territorial.

# Elaboração de gráficos no Power BI com dados da ANTT

<img width="1162" height="734" alt="image" src="https://github.com/user-attachments/assets/81a78eac-7da1-48e2-901e-fb580331a2e1" />

Após finalizar o trabalho com os dados da ANTT no Excel, passei a utilizar essa mesma base no Power BI. Durante essa atividade, comecei a explorar novas formas de apresentar os dados, utilizando gráficos e recursos interativos para facilitar a visualização das informações. Também pude conhecer melhor o processo de criação e organização de relatórios na plataforma. Essa etapa foi importante para perceber as diferenças entre o Excel e o Power BI. Enquanto o Excel permite organizar e analisar os dados de forma prática, o Power BI oferece mais recursos para criar visualizações dinâmicas e interativas, tornando a interpretação dos resultados mais simples e eficiente.

# Elaboração de gráficos no Power BI com os dados dos municípios de São Paulo

<img width="1314" height="743" alt="image" src="https://github.com/user-attachments/assets/ca6b93cf-97f9-4c4c-869d-1a007bbd420c" />

Na última atividade, eu utilizei a base de dados dos municipios de São Paulo , mas dessa vez trabalhei diretamente no Power BI.
Diferente da atividade que eu tinha feito antes no Excel, nessa etapa eu criei os gráficos primeiro e, a partir deles, fui elaborando perguntas que poderiam ser respondidas com as informações apresentadas.
Essa atividade foi importante porque reuniu várias coisas que eu já tinha aprendido nas atividades anteriores, como análise de dados, criação de perguntas, utilização de gráficos e interpretação das informações.
No final, consegui perceber melhor a evolução entre trabalhar com uma planilha simples no Excel e depois transformar esses mesmos dados em gráficos e relatórios mais interativos no Power BI.


# Atividade - Regressão Linear Simples

## Nupcialidade

Análise da relação entre a idade média dos homens e das mulheres ao casar.

- Variável X: Idade média dos homens.
- Variável Y: Idade média das mulheres.
- R²: 0,9384.
- Equação: y = 1,0284x - 3,6951.

## Gráfico de dispersão

<img width="983" height="657" alt="Captura de tela 2026-11-13 194024" src="https://github.com/user-attachments/assets/5364a843-1ad5-4185-bc1c-7a9789703f67" />


## Conclusão

O modelo de regressão linear se aplica ao caso, pois o R² é próximo de 1, indicando forte relação linear positiva entre as variáveis.

## Regressão linear
Neste trabalho, fizemos um estudo, para que fosse identificado dados que relacionassem horas de estudo, com resultados em provas e testes.
Ao utilizar o google colab, pude montar um modelo de regressão linear.

          },
          "metadata": {}
        },
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "\n",
            "RESULTADOS DA REGRESSÃO LINEAR\n",
            "Coeficiente angular: 0.7967\n",
            "Intercepto: 1.9327\n",
            "\n",
            "Equação da reta:\n",
            "Nota = 1.9327 + 0.7967 × Horas de estudo\n",
            "\n",
            "R² = 0.9964\n"
          ]
        },
        {
          "output_type": "display_data",
          "data": {
            "text/plain": [
              "<Figure size 900x600 with 1 Axes>"
            ],
           
          },
          "metadata": {}
        },
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "\n",
            "CONCLUSÃO\n",
            "Sim! Mais horas de estudo estão associadas a notas maiores.\n",
            "O valor de R² é 0.9964, indicando um ajuste muito forte.\n"
          ]
        }
      ],
      "source": [
        "\n",
        "# ============================================\n",
        "# ATIVIDADE: REGRESSÃO LINEAR\n",
        "# HORAS DE ESTUDO X NOTA DA PROVA\n",
        "# ============================================\n",
        "\n",
        "# 1. Importar bibliotecas\n",
        "import pandas as pd\n",
        "import numpy as np\n",
        "import matplotlib.pyplot as plt\n",
        "from sklearn.linear_model import LinearRegression\n",
        "from sklearn.metrics import r2_score\n",
        "\n",
        "# 2. Criar a base de dados\n",
        "dados = {\n",
        "    'Horas de estudo': [1, 2, 2.5, 3, 4, 4.5,\n",
        "                        5, 6, 6.5, 7, 8, 9],\n",
        "\n",
        "    'Nota da prova': [2.8, 3.5, 4.0, 4.2, 5.0, 5.7,\n",
        "                      6.0, 6.6, 7.1, 7.3, 8.4, 9.2]\n",
        "}\n",
        "\n",
        "df = pd.DataFrame(dados)\n",
        "\n",
        "# 3. Mostrar a tabela\n",
        "print(\"BASE DE DADOS\")\n",
        "display(df)\n",
        "\n",
        "# 4. Separar as variáveis X e Y\n",
        "X = df[['Horas de estudo']]\n",
        "y = df['Nota da prova']\n",
        "\n",
        "# 5. Criar e treinar o modelo\n",
        "modelo = LinearRegression()\n",
        "modelo.fit(X, y)\n",
        "\n",
        "# 6. Realizar previsões\n",
        "previsoes = modelo.predict(X)\n",
        "\n",
        "# 7. Calcular o R²\n",
        "r2 = r2_score(y, previsoes)\n",
        "\n",
        "# 8. Mostrar os resultados\n",
        "print(\"\\nRESULTADOS DA REGRESSÃO LINEAR\")\n",
        "\n",
        "print(f\"Coeficiente angular: {modelo.coef_[0]:.4f}\")\n",
        "print(f\"Intercepto: {modelo.intercept_:.4f}\")\n",
        "\n",
        "print(f\"\\nEquação da reta:\")\n",
        "print(f\"Nota = {modelo.intercept_:.4f} + {modelo.coef_[0]:.4f} × Horas de estudo\")\n",
        "\n",
        "print(f\"\\nR² = {r2:.4f}\")\n",
        "\n",
        "# 9. Criar gráfico de dispersão\n",
        "plt.figure(figsize=(9, 6))\n",
        "\n",
        "plt.scatter(\n",
        "    X['Horas de estudo'],\n",
        "    y,\n",
        "    color='blue',\n",
        "    label='Notas dos alunos',\n",
        "    s=70\n",
        ")\n",
        "\n",
        "# Adicionar a reta de regressão\n",
        "plt.plot(\n",
        "    X['Horas de estudo'],\n",
        "    previsoes,\n",
        "    color='red',\n",
        "    label='Linha de regressão'\n",
        ")\n",
        "\n",
        "plt.title('Regressão Linear: Horas de Estudo x Nota da Prova')\n",
        "plt.xlabel('Horas de estudo')\n",
        "plt.ylabel('Nota da prova')\n",
        "plt.legend()\n",
        "plt.grid(True)\n",
        "\n",
        "plt.show()\n",
        "\n",
        "# 10. Conclusão\n",
        "print(\"\\nCONCLUSÃO\")\n",
        "\n",
        "if modelo.coef_[0] > 0:\n",
        "    print(\"Sim! Mais horas de estudo estão associadas a notas maiores.\")\n",
        "else:\n",
        "    print(\"Não! Não foi encontrada uma associação positiva.\")\n",
        "\n",
        "print(f\"O valor de R² é {r2:.4f}, indicando um ajuste muito forte.\")\n"
      ]
    }
  ]
}

## Nesta imagem podemos visualizar o gráfico com a relação dos dados e os resultados apresentados:

<img width="1073" height="378" alt="image" src="https://github.com/user-attachments/assets/a761cc6d-3983-4283-ac18-9278df302f40" />

## Conclusão
Sim, Mais horas de estudo estão associadas a notas maiores.
O valor de R² é 0.9964, indicando um ajuste muito forte.

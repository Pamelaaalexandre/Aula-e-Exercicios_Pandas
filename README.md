# 🎸 Análise de Dados de Shows e Eventos com Pandas

Este projeto consiste em uma análise exploratória de dados de shows e eventos utilizando a biblioteca **Pandas** em Python. O objetivo principal foi compreender a distribuição de ingressos vendidos, faturamento por evento, taxa de ocupação dos locais e extrair insights valiosos sobre o desempenho de diferentes artistas e cidades.

---

## 📊 Sobre os Dados

A base de dados original (`shows_eventos.csv`) contém as seguintes informações sobre 20 eventos:
- **ID_Show**: Identificador único do evento.
- **Artista**: Nome do artista ou banda.
- **Genero**: Gênero musical do show.
- **Cidade**: Cidade onde ocorreu a apresentação.
- **Ingressos_Vendidos**: Quantidade total de ingressos comprados.
- **Capacidade_Local**: Capacidade máxima de público do local do evento.
- **Preco_Medio_Ingresso**: Preço médio cobrado por ingresso.

---

## 🛠️ Tecnologias Utilizadas

- **Python 3**
- **Pandas**: Para manipulação e análise exploratória de dados.
- **Google Colab / Jupyter Notebook**: Ambientes de desenvolvimento.

---

## 📈 Etapas da Análise Realizada

### 1. Importação das Bibliotecas e Leitura de Dados
Os dados foram carregados a partir de um arquivo CSV para um DataFrame Pandas utilizando o método `pd.read_csv()`.

### 2. Análise Descritiva e Ficha Técnica
- Utilizamos o método `.info()` para verificar os tipos de variáveis e garantir que não houvesse dados nulos.
- Aplicamos o método `.describe()` para realizar uma análise quantitativa (médias, mínimos, máximos de ingressos e preços).
- Com `.describe(include="object")`, analisamos qualitativamente as colunas de texto para identificar que o gênero mais frequente nos eventos foi o **Pop** e a cidade com mais shows foi **São Paulo**.

### 3. Engenharia de Recursos (Feature Engineering)
Criamos novas métricas fundamentais para o negócio:
- **Receita Gerada**: Calculada multiplicando a quantidade de ingressos vendidos pelo preço médio do ingresso.
  $$\text{Receita} = \text{Ingressos Vendidos} \times \text{Preço Médio}$$
- **Taxa de Ocupação (%)**: Percentual de preenchimento do local do evento.
  $$\text{Taxa de Ocupação} = \left( \frac{\text{Ingressos Vendidos}}{\text{Capacidade Local}} \right) \times 100$$

### 4. Exportação dos Resultados
Após enriquecer a base de dados com as novas métricas, exportamos o resultado final para um novo arquivo estruturado chamado `shows_eventos_novo.csv` utilizando o método `.to_csv()`.

---

## 🚀 Como Executar o Projeto

1. Certifique-se de ter o Python e o Pandas instalados na sua máquina:
   ```bash
   pip install pandas
   ```
2. Clone este repositório:
   ```bash
   git clone https://github.com/seu-usuario/nome-do-seu-repositorio.git
   ```
3. Garanta que o arquivo `shows_eventos.csv` esteja na mesma pasta do script/notebook.
4. Execute o notebook ou script Python para visualizar os resultados e gerar o novo arquivo consolidado.

---

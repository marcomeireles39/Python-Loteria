# Python-Loteria
 Projeto python com classe e programa para pegar numeros de jogos

Primeiro projeto de meu repositório criado dia 31-02-2022 que consiste
em uma classe que possibilita a extração de dados relativos aos jogos
legalizados no Brasil.

Essa classe consegue pegar dados dos sorteios das loterias:
- MEGA SENA
- LOTO FÁCIL
- QUINA
- LOTO MANIA
- TIME MANIA
- DUPLA SENA
- DIA DE SORTE
- SUPER SETE

caixa.py
O arquivo caixa.py contem a classe Loterias com metodos que irão capturar
os dados dos jogos citados acima de forma simples

Classes utilizadas

import requests
- Requisição de conexão com o site específico

from bs4 import BeautifulSoup
- Extração e normatização dos dados

import json
- Normalização dos dados

Quais dados serão extraidos

- Tipo de Jogo

- Numero do concurso

- Município do sorteio

- Data de apuração

- Valor da arrecadação

- Valor estimado para proximo concurso

- Valor acumulado para o proximo concurso

- Valor acumulado para o concurso especial

- Se acumulou para o proximo concurso

- Indicador do concurso especial

- Dezenas sortadas por ordem de sorteio

- lista de municípios ganhadores

- lista de rateio de prêmios

Como funciona:

Primeiro importe a classe para ser usada no projeto

codigo:

from caixa import Loterias


depois vamos criar uma instancia da classe

codigo:

id_obj = Loterias(tipo)

Parametro tipo:
"mega-sena"
"loto-facil"
"quina"
"loto-mania"
"time-mania"
"dupla-sena"
"dia-de-sorte"
"super-sete"

Exemplo:

        id_obj = Loterias("mega-sena") - Metodo construtor que receberá o tipo de loteria que será trabalhada

<h3>Lista de metodos para acesso:</h3>






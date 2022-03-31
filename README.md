# Python-Loteria

<h1> Projeto python com classe e programa para pegar numeros de jogos</h1>

Primeiro projeto de meu repositório criado dia 31-02-2022 que consiste
em uma classe que possibilita a extração de dados relativos aos jogos
legalizados no Brasil.

<b>Essa classe consegue pegar dados dos sorteios das loterias:

- MEGA SENA
- LOTO FÁCIL
- QUINA
- LOTO MANIA
- TIME MANIA
- DUPLA SENA
- DIA DE SORTE
- SUPER SETE

<b><i>caixa.py</i></b>

<p>O arquivo caixa.py contem a classe Loterias com metodos que irão capturar
os dados dos jogos citados acima de forma simples
</p>

<h2>Classes utilizadas</h2>

<i> Codigo</i>
import requests
- Requisição de conexão com o site específico

from bs4 import BeautifulSoup
- Extração e normatização dos dados

import json
- Normalização dos dados

<b>Quais dados serão extraidos</b>

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

<b>Como funciona</b>:

Primeiro importe a classe para ser usada no projeto

<i>codigo:</i>

from caixa import Loterias


depois vamos criar uma instancia da classe

<i>codigo:</i>

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

<i>Exemplo:</i>

        id_obj = Loterias("mega-sena") - Metodo construtor que receberá o tipo de loteria que será trabalhada

<h3>Lista de metodos para acesso:</h3>

 <i> Codigo: </i>

    id_obj.buscar(nconcurso)

<b>Parametro nconcurso:</b> Numero do concurso ao qual eu procuro os dados.

<b>Observação</b>

<p>O metodo buscar é um dos mais importantas pois é ele que vai acessar todos os dados do jogo especifico
e vai retornar a classe , os outros metodos retornam o valor para a apresentação , são eles:</p>

  <b>retorna =  id_obj.tipo_jogo()</b> - <i>Retorna o id de identificação do tipo de jogo</i>
  
<b>retorna =  id_obj.concurso()</b> - <i>Retorna o numero do concurso</i>

<b>retorna =  id_obj.Municipio_Sorteio()</b> - <i>Retorna o município de realização do concurso</i>

<b>retorna =  id_obj.DataApuracao()</b> - <i>Retorna a data do concurso</i>

<b>retorna =  id_obj.ValorArrecadado()</b> - <i>Retorna o valor arrecadado até o concurso</i>

<b>retorna =  id_obj.ValorEstimadoProximoConcurso()</b> - <i>Retorna o valor estimado para o proximo concurso</i>

<b>retorna =  id_obj.ValorAcumuladoProximoConcurso()</b> - <i>Retorna o valor acumulado para o próximo concurso</i>

<b>retorna =  id_obj.ValorAcumuladoConcursoEspecial()</b> - <i>Retorna o valor acumulado para o concurso especial</i>

<b>retorna =  id_obj.ValorAcumuladoConcurso_0_5</b> - <i> Retorna o valor acumulado de concurso - a 5</i>

<b>retorna =  id_obj.Acumulado</b> - <i>Retorna valor booleano se acumulou ou no caso nao houve vencedor</i>

<b>retorna =  id_obj.IndicadorConcursoEspecial</b> - <i> Retorna o indicador de concurso especial</i>

<b>retorna =  id_obj.DezenasSorteadasOrdemSorteio</b> - <i>Retorna as Dezenas sorteadas em formato de lista</i>

<b>retorna =  id_obj.ListaMunicipioUFGanhadores</b> - <i>Retorna os municipios ganhadores em formato de lista</i>

<b>retorna =  id_obj.ListaRateioPremio</b> - <i>Retorna uma lista com os dados de numero de acertos, numero,

numero de ganhadores, valor do premio unitario e a descricao</i>


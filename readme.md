<h1> Dashboard Fórmula 1 </h1>

<h3> Análise exploratória de pilotos e equipes de fórmula 1 no período de 2007 à 20017. E pode ser acessado através do link abaixo,

[Dashboard - Fórmula 1](https://app.powerbi.com/links/XPxnhOJVJB?ctid=b1051c4b-3b94-41ab-9441-e73a72342fdd&pbi_source=linkShare)



<h2><br>Medidas</h2>
<ul>
    <li>Temporadas: Quantidade de temporadas que participou. [Pilotos e Equipes] </li>
    <li>Total de Corridas: Quantidade de corridas que participou. [Pilotos e Equipes]</li>
    <li>1º Lugar: Quantidade de vezes que venceu a corrida. [Pilotos e Equipes]</li>
    <li>2º Lugar: Quantidade de vezes que ficou em segundo lugar na corrida. [Pilotos e Equipes]</li>    
    <li>3º Lugar: Quantidade de vezes que ficou em terceiro lugar na corrida. [Pilotos e Equipes]</li>
    <li>Podium: Quantidade de vezes que ocupou o podium na corrida. [Pilotos e Equipes]</li>
    <li>Taxa de vitória: Porcentagem relativa a quantidade de vezes que venceu as corridas que participou. [Pilotos e Equipes]</li>
    <li>Taxa Segundo Lugar: Porcentagem relativa a quantidade de vezes que ficou em segundo lugar nas corridas que participou. [Pilotos e Equipes]</li>
    <li>Taxa Terceiro Lugar: Porcentagem relativa a quantidade de vezes que ficou em terceiro lugar nas corridas que participou. [Pilotos e Equipes]</li>
    <li>Taxa Podium: Porcentagem relativa a quantidade de vezes que ocupou o podium nas corridas que participou. [Pilotos e Equipes]</li>
    <li>Pontos Primeiro Colocado: Quantidade de pontos do primeiro colocado da temporada. [Pilotos]</li>
    <li>Pontos Primeira Colocada: Quantidade de pontos do primeiro colocado da temporada. [Equipes]</ii>
    <li>Pontos Ranking: Somatória de pontos para cálculo do ranking. [Pilotos e Equipes]</li>
    <li>Ranking Pontos: Rankear conforme pontuação. [Pilotos</li>
    <li>Rank - Equipes (pts): Rankear conforme pontuação. [Equipes] </li>
    <li>Ranking Temporada: Rankear conforme pontos e temporada. [Pilotos e Equipes]</li>
    <li>Campeão: Quantidade de vezes que venceu a temporada. [Pilotos e Equipes]</li>
    <li>Vice Campeão: Quantidade de vezes que ficou em segundo lugar na temporada. [Pilotos e Equipes]</li>
    <li>Terceiro Lugar: Quantidade de vezes que ficou em terceiro lugar na temporada. [Pilotos e Equipes]</li>
    <li>Melhor tempo por volta: Tempo da volta mais rápida realizada. [Pilotos]</li>
    <li>Velocidade da melhor volta: Velocidade da volta mais rápida realizada. [Pilotos]</li>
</ul>
<h3>Nota: As medidas de taxa (Podium, 1º, 2º e 3º Lugar ) quando aplicadas as equipes demonstram a porcetagem de vezes que a equipe ocupou tais posições e não a porcetagem em relação as possibilidades)</h3>
<h3>Exemplo:</h3>
<ul>
    <li>Equipe: ABC
    <li>Qtde Corridas: 1
    <li>Pilotos:
    <ul>
        <li>Piloto Z - 2º Lugar (Podium)
        <li>Piloto W - 4º Lugar
    </ul>
</ul>
<h3>Assim temos que para 1 corrida, 1 podium. Portando, "Taxa Podium"  = 100%. A equipe apareceu no podium 100% das corridas, porém o aproveitamento efetivo seria de 50%, pois a equipe possui 2 pilotos.</h3>

<h2> <br> Relacionamentos </h2>
<ul>
    <li>dim_circuits_v1[circuitId] ➜ dim_races[circuitId] (1:*) </li>
    <li>dim_season[year] ➜ dim_races[year] (1:*)</li>
    <li>dim_races[raceId] ➜ constructorStandings[raceId] (1:*) </li>
    <li>dim_races[raceId] ➜ constructorResults[raceId] (1:*) </li>
    <li>dim_races[raceId] ➜ results_v1[raceId] (1:*) </li>
    <li>dim_races[year] ➜ Tabela_Aux[year] (*:*) </li>
    <li>dim_constructors[constructorId] ➜ constructorStandings[constructorId] (1:*)</li>
    <li>dim_constructors[constructorId] ➜ constructorResults[constructorId] (1:*)</li>
    <li>dim_constructors[constructorId] ➜ results_v1[constructorId] (1:*)</li>
    <li>dim_drivers_v1[driverId] ➜ Tabela_Aux[driverId] (1:*)</li>
    <li> dim_driver_v1[driverId] ➜ results_v1[driverId] (*:*) </li>
</ul>

<h2> <br> Tratamento dos dados </h2>
<h3> Análise e tratamentos da base de dados e realizado com python,  </h3> 

[Scripts](https://github.com/Hiraee/Formula1/tree/main/Scripts_TratamentoDados) 

<ul>
    <li><h3>Bibliotecas</h3></li>
    <ul>
        <li>pandas</li>
        <li>magic</li>
        <li>re</li>
    </ul>
</ul>

# F1-Prediction-Model

Teams & Drivers:
1. Aston Martin - Lance Stroll & Fernando Alonso
2. Alpine - Pierre Gasly & 
3. Ferrari - Charles Leclerc & Lewis Hamilton
4. Haas
5. Kick Sauber
6. McLaren - Oscar Piastri & Lando Norris
7. Mercedes - George Russell & Kimi Antonelli
8. Racing Bulls
9. Red Bull Racing - Max Verstappen & Yuki Tsunoda
10. Williams

ML Algo: Random Forest

Data Needed (for each Driver):
Starting position - results.['GridPosition'],
Finishing position - results.['Position'],
Classified position (relevant for DNF data) - results.['ClassifiedPosition'],
Championship points for relevant races (2) - Dutch.results.['Points'] + Hungary.results.['Points'],
Team standing in Contructors Championship for relevant races (2) - Dutch.results.['Points'] + Hungary.results.['Points'].

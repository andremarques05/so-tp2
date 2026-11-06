# Resultados das simulações (escalonador FIFO)

Faltas de página = acessos a páginas que não estavam em RAM (inclui a 1.ª vez que cada página é usada). Swap-in = leituras do disco; swap-out = escritas no disco (só páginas sujas). RANDOM: média de 5 execuções (`--seed 1..5`), com o intervalo mín–máx.

## Cenário `02_localidade`

Ficheiro(s): 02_localidade.csv  
Argumentos: `--vpages 30 --pframes 14 --threshold 2`

| Algoritmo | Acessos | Page faults | Swap-in (leituras) | Swap-out (escritas) | Swap total | Taxa de faltas |
|---|---|---|---|---|---|---|
| FIFO | 264 | 168 | 138 | 50 | 188 | 0.636 |
| RANDOM | 264 | 143.0 (141–149) | 113.0 (111–119) | 44.6 (41–47) | 157.6 (152–165) | 0.542 |
| LRU | 264 | 80 | 50 | 22 | 72 | 0.303 |
| NRU | 264 | 80 | 50 | 22 | 72 | 0.303 |
| CLOCK | 264 | 96 | 66 | 32 | 98 | 0.364 |

## Cenário `03_varrimento_ciclico`

Ficheiro(s): 03_varrimento_ciclico.csv  
Argumentos: `--vpages 30 --pframes 14 --threshold 2`

| Algoritmo | Acessos | Page faults | Swap-in (leituras) | Swap-out (escritas) | Swap total | Taxa de faltas |
|---|---|---|---|---|---|---|
| FIFO | 120 | 120 | 96 | 34 | 130 | 1.000 |
| RANDOM | 120 | 99.6 (97–102) | 75.6 (73–78) | 31.8 (30–34) | 107.4 (103–110) | 0.830 |
| LRU | 120 | 120 | 96 | 34 | 130 | 1.000 |
| NRU | 120 | 120 | 96 | 34 | 130 | 1.000 |
| CLOCK | 120 | 120 | 96 | 34 | 130 | 1.000 |

## Cenário `04_zipf_misto`

Ficheiro(s): 04_zipf_misto.csv  
Argumentos: `--vpages 30 --pframes 14 --threshold 2`

| Algoritmo | Acessos | Page faults | Swap-in (leituras) | Swap-out (escritas) | Swap total | Taxa de faltas |
|---|---|---|---|---|---|---|
| FIFO | 240 | 87 | 60 | 52 | 112 | 0.362 |
| RANDOM | 240 | 85.8 (85–87) | 58.8 (58–60) | 48.0 (44–53) | 106.8 (103–113) | 0.357 |
| LRU | 240 | 71 | 44 | 39 | 83 | 0.296 |
| NRU | 240 | 69 | 42 | 38 | 80 | 0.287 |
| CLOCK | 240 | 75 | 48 | 43 | 91 | 0.312 |

## Cenário `05_duas_apps`

Ficheiro(s): 02_localidade.csv + 04_zipf_misto.csv (2 aplicações em simultâneo)  
Argumentos: `--vpages 30 --pframes 20 --threshold 2`

| Algoritmo | Acessos | Page faults | Swap-in (leituras) | Swap-out (escritas) | Swap total | Taxa de faltas |
|---|---|---|---|---|---|---|
| FIFO | 504 | 279 | 222 | 106 | 328 | 0.554 |
| RANDOM | 504 | 251.2 (231–259) | 194.2 (174–202) | 92.0 (86–98) | 286.2 (262–294) | 0.498 |
| LRU | 504 | 173 | 116 | 66 | 182 | 0.343 |
| NRU | 504 | 173 | 116 | 66 | 182 | 0.343 |
| CLOCK | 504 | 184 | 127 | 76 | 203 | 0.365 |

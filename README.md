# 2022-RSK-Nups-VIRO
This repo contains datasets and R scripts that were used to obtain the results described in the following submitted article :

> *Cardiovirus leader proteins retarget RSK kinases toward alternative substrates to perturb nucleocytoplasmic traffic* Belén Lizcano-Perret; Cécile Lardinois; Fanny Wavreil; Philippe Hauchamps; Gaëtan Herinckx; Frédéric Sorgeloos; Didier Vertommen; Laurent Gatto; Thomas Michiels


traffic.

- Rmd scripts are stored in the main directory, together with html outputs. 
- Dumps of intermediary R objects are stored in /rds directory. This allows to keep intermediary results in order to speed up the run of the script. 
However, if one would like to re-launch (parts of) the computations from scratch, one just need to delete (or rename) the corresponding .rds objects, and re-launch the .rmd scripts.
- Datasets are stored in /data directory. Additional information needed to interpret the datasets is provided herebelow.

MASSPROT experiment numbers:
- BioID-L: VIRO488 and VIRO523
- BioID-RSK: VIRO473 and VIRO523

### Experimental design

| NI            | WT (R02)      | M60V (R02)    | F48A          | Replicate |   |
|---------------|---------------|---------------|---------------|-----------|---|
| VIRO488_A3    | VIRO488_B3    | VIRO488_C3    | VIRO488_D3    | 1         | L |
| VIRO488_A2    | VIRO488_B2    | VIRO488_C2    | VIRO488_D2    | 1         | L |
| VIRO488_A1    | VIRO488_B1    | VIRO488_C1    | VIRO488_D1    | 1         | L |
| VIRO523_L1_01 | VIRO523_L1_02 | VIRO523_L1_03 | VIRO523_L1_04 | 2         | L |
| VIRO523_L1_05 | VIRO523_L1_06 | VIRO523_L1_07 | VIRO523_L1_08 | 2         | L |
| VIRO523_L1_09 | VIRO523_L1_10 | VIRO523_L1_11 | VIRO523_L1_12 | 2         | L |
| VIRO523_L2_01 | VIRO523_L2_02 | VIRO523_L2_03 | VIRO523_L2_04 | 3         | L |
| VIRO523_L2_05 | VIRO523_L2_06 | VIRO523_L2_07 | VIRO523_L2_08 | 3         | L |
| VIRO523_L2_09 | VIRO523_L2_10 | VIRO523_L2_11 | VIRO523_L2_12 | 3         | L |
| VIRO473_A3    | VIRO473_B3    | VIRO473_C3    |               | 1         | R |
| VIRO473_A2    | VIRO473_B2    | VIRO473_C2    |               | 1         | R |
| VIRO473_A1    | VIRO473_B1    | VIRO473_C1    |               | 1         | R |
| VIRO523_R1_01 | VIRO523_R1_02 | VIRO523_R1_03 |               | 2         | R |
| VIRO523_R1_04 | VIRO523_R1_05 | VIRO523_R1_06 |               | 2         | R |
| VIRO523_R1_07 | VIRO523_R1_08 | VIRO523_R1_09 |               | 2         | R |
| VIRO523_R2_01 | VIRO523_R2_02 | VIRO523_R2_03 |               | 3         | R |
| VIRO523_R2_04 | VIRO523_R2_05 | VIRO523_R2_06 |               | 3         | R |
| VIRO523_R2_07 | VIRO523_R2_08 | VIRO523_R2_09 |               | 3         | R |

- L-Experiment: MaxQuant analysis: 20191129 on windows computer: L: WT + M60V + F48A
- R-Experiment : MaxQuant analysis: 20191218 on windows computer : R : WT + M60V

### Comment on reproducibility of results
Re-run from scratch of the computations with more recent versions of proDA might lead to slightly different outcomes (e.g. an impact on 4th digit - or further - on p-values has been seen), 
but should not change the conclusions of the analysis, i.e. order of differentially abundant proteins and shape of volcano plots.

##Sequencer Output to Diversity Analysis (SODA) [2nd Half]

### Author:
Ruben Rodriguez <br>
rubenrr7@outlook.com

### Program Work Flow:
1. Visualization of Alpha Diversity as a function of sampling depth
2. Explore sample composition using taxonomic classifier
3. Generate interactive taxonomic sample plots 
4. Differentiate sample group abundances using ANCOM

### Dependencies:
- Hoffman
- Python
- Quiime 2 (can be loaded into terminal using python anaconda2
- classifier.qza

### Instructions:
1. You need to make sure you are on the main directory in which you are runnning your created program.
2. You need to have the following plugin in your directory:
- classifier.qza

You can obtain this plugin by using the following commands:

```{bash}
wget \
  -O "gg-13-8-99-515-806-nb-classifier.qza" \
  "https://data.qiime2.org/2019.1/common/gg-13-8-99-515-806-nb-classifier.qza"
  ```
3. You can use nano to copy and paste the master script called master 2nd part, which is which is in the directory mastscript on this github, into a bash script on your terminal. 

4. You can then just enter the following command:

```{bash}
sh master.sh -i emp-single-end-sequences/ -o output-emp-single-end-sequences -m sample-metadata.tsv -x demultiplex-sequences/ -v visuals/ -a dada2/ -t table-dada2/ -s stats-dada2/ -n aligned-sequences/ -u unrooted-tree/ -r rooted-tree/ -c core-metrics-results/
```

5. In order for you to be able to see your visuals that you have created (either .qza/.qzv) you will have to go ahead and copy them ont your desktop and the drag them from there onto QIIME2 View (https://view.qiime2.org). You may also use Cyberduck to transfer them files from your desktop. 

### Expected Ouputs:
The following directories are expected to be outputs in one master directory:

table <br>
└──  gut-table.qza <br>
└──  comp-gut-table.qza <br>
└──  gut-table-l6.qza <br>
└──  comp-gut-table-l6.qza <br>

taxonomy <br>
└── taxonomy.qza <br>

classifier <br>
└── gg-13-8-99-515-806-nb-classifier.qza <br>

visuals <br>
└── alpha-rarefaction.qzv <br>
└── taxonomy.qzv <br>
└── taxa-bar-plots.qzv <br>
└── ancom-Subject.qzv <br>
└── l6-ancom-Subject.qzv <br>

### Citing:
_CitingSODA_ doi: 10.5281/zenodo.3245509


### References:

1. QIIME2 development team. 2016-2019. “Moving Pictures” tutorial. QIIME2 docs. <https://docs.qiime2.org/2019.4/tutorials/moving-pictures/>
4. Bolyen E, Rideout JR, Dillon MR, Bokulich NA, Abnet C, Al-Ghalith GA, Alexander H, Alm EJ, Arumugam M, Asnicar F, Bai Y, Bisanz JE, Bittinger K, Brejnrod A, Brislawn CJ, Brown CT, Callahan BJ, Caraballo-Rodríguez AM, Chase J, Cope E, Da Silva R, Dorrestein PC, Douglas GM, Durall DM, Duvallet C, Edwardson CF, Ernst M, Estaki M, Fouquier J, Gauglitz JM, Gibson DL, Gonzalez A, Gorlick K, Guo J, Hillmann B, Holmes S, Holste H, Huttenhower C, Huttley G, Janssen S, Jarmusch AK, Jiang L, Kaehler B, Kang KB, Keefe CR, Keim P, Kelley ST, Knights D, Koester I, Kosciolek T, Kreps J, Langille MG, Lee J, Ley R, Liu Y, Loftfield E, Lozupone C, Maher M, Marotz C, Martin BD, McDonald D, McIver LJ, Melnik AV, Metcalf JL, Morgan SC, Morton J, Naimey AT, Navas-Molina JA, Nothias LF, Orchanian SB, Pearson T, Peoples SL, Petras D, Preuss ML, Pruesse E, Rasmussen LB, Rivers A, Robeson, II MS, Rosenthal P, Segata N, Shaffer M, Shiffer A, Sinha R, Song SJ, Spear JR, Swafford AD, Thompson LR, Torres PJ, Trinh P, Tripathi A, Turnbaugh PJ, Ul-Hasan S, van der Hooft JJ, Vargas F, Vázquez-Baeza Y, Vogtmann E, von Hippel M, Walters W, Wan Y, Wang M, Warren J, Weber KC, Williamson CH, Willis AD, Xu ZZ, Zaneveld JR, Zhang Y, Zhu Q, Knight R, Caporaso JG. 2018. QIIME 2: Reproducible, interactive, scalable, and extensible microbiome data science. PeerJ Preprints 6:e27295v2 https://doi.org/10.7287/peerj.preprints.27295v2
5. Python Software Foundation. Python Language Reference, version 2.7. Available at <http://www.python.org>
6. Anaconda Software Distribution. Computer software. Vers. 2-2.4.0. Anaconda, Nov. 2016. Web. <https://anaconda.com> 

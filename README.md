# GWAS_causalEffects_extendedModel
https://www.biorxiv.org/content/10.1101/705285v2

All code requires Matlab.

All original data is publicly available and described in the paper.

(1) Build linkage disequilibrium histogram and heterozygosity for each SNP using 1000 Genomes data and buildLDhistAndTLD_A.m

(2) Choose a phenotype in causalEffectsModelDriver11m.m; Choose an outDir; Process once with
    	   RESTART_AT_BC = false;
    	   fancyMinFracOfYmax = 0.999;
(3)  Then restart with restartInDir set to previous outDir, choosing a new outDir this time; Use
    	   RESTART_AT_BC = true;
    	   fancyMinFracOfYmax = 0.01;
(4) Results in final outDir can be visualized using makePhenoQQfigs.m

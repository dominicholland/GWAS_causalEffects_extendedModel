# GWAS_causalEffects_extendedModel
https://www.biorxiv.org/content/10.1101/705285v2

All code requires Matlab. Results obtained using R2015b.

All original data is publicly available and described in the paper.

(1) Build linkage disequilibrium histogram and heterozygosity for each SNP for an approximately 11 million SNP reference panel using 1000 Genomes data and buildLDhistAndTLD_A.m. Relies on PlinkRead_binary.m

(2) Choose a phenotype in causalEffectsModelDriver11m.m; Choose an outDir; Process once with
    	   RESTART_AT_BC = false;
    	   fancyMinFracOfYmax = 0.999;
(3)  Then restart with restartInDir set to previous outDir, choosing a new outDir this time; Use
    	   RESTART_AT_BC = true;
    	   fancyMinFracOfYmax = 0.01;
(4) Results in final outDir can be visualized using makePhenoQQfigs.m

Runtime is approximately 12 hours.

causalEffectsModelDriver11m.m relies on GenStats_QQ_plot_withCI.m, histmean_dh.m, causalEffectsModelCost_fourier.m, mnpdfln.m, my_sigmoid.m, my_sigmoid_positive.m, my_sigmoid_positive_fancy.m;

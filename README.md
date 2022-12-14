# Cryptosporidium

In progress: Please contact Joe Campo (Joe Campo <jcampo@antigendiscovery.com>) for specific information on executing this analysis and to obtain the final scripts


Genome wide identification of Cryptosporidium cell surface and secreted proteins associated with humoral immunity to reinfection

ClinicalTrials.gov identifier NCT02764918. “Cryptosporidiosis and Enteropathogens in Bangladesh”
dbGAP Accession phs001665.v1.p1!


Statistical Analysis
Cryptosporidium protein responses were classified as seropositive or negative by taking the distribution of each spot individually between all samples to model negative and positive subpopulations using mixture models executed with the “normalmixEM” function in the mixtools package  and a seropositivity cutoff was established for each antigen as the mean and three standard deviations of the negative SI distribution. When mixture models failed to converge, a simple seropositivity cutoff of 1.0, or 2-fold over background, was applied. IgG and IgA “reactivity” for each antigen was defined as a proportion of seropositive responses, or seroprevalence, of at least 10% among the study children. Overlap in IgG and IgA responses that recognized individual antigens was assessed using the UpSetR package. Antibody breadth scores were calculated as the sum of seropositive responses per individual. Normalized SI and antibody breadth scores were visualized using the ComplexHeatmap package.  Associations between normalized SI and protein features such as life cycle stage and signal peptides were analyzed using multivariable negative binomial regression for seropositivity classifications and ordinary least squares regression for normalized SI. Univariate groupwise analysis was performed using T-tests. Correlations were assessed using Pearson’s correlation coefficient. Unsupervised data reduction and trends was analyzed using t-distributed stochastic neighbor embedding (tSNE), using a perplexity parameter of 40, 1000 iterations and a theta of 0.0 after testing varying parameters for shape of the data to test differences in profile-wide normalized SI and to control for multiple measurements per subject, linear mixed effects regression (LMER) was used with the lme4 package , allowing for random intercepts at the subject and antigen level—p-values for LMER models were obtained by ANOVA between full models and null variable models. Supervised data reduction and multi-antigen analysis was performed using partial least squares discriminant analysis (PLS-DA) using the mixOmics package (65). Analysis of antibody breadth was performed using negative binomial regression. Analysis of seropositivity to an antigen and association with risk of infection, reinfection or diarrheal illness during the one-year and two-year follow-up periods following sample collection was performed using Cox proportional hazards models adjusted by the number of episodes a child had, HAZ score at birth, mother’s age, BMI and education level, household income and expenses, principal source of household drinking water, the water treatment method routinely used by the household, proximity to one of the Dhaka water drainage channels . 

RStudio Team. RStudio: Integrated Development for R. [Internet]2015;http://www.rstudio.com/. cited August 7, 2022!

Benaglia T, Chauveau D, Hunter DR, Young D. mixtools : An R Package for Analyzing Finite Mixture Models. J Stat Softw 2009;32(6). doi:10.18637/jss.v032.i06![
van der Maaten L, Courville A, Fergus R, Manning C. Accelerating t-SNE using Tree-Based Algorithms [Internet]. 2014!

Lex A, Gehlenborg N. Sets and intersections. Nat Methods 2014;11(8):779–779.

Lex A, Gehlenborg N, Strobelt H, Vuillemot R, Pfister H. UpSet: Visualization of Intersecting Sets.. IEEE Trans Vis Comput Graph 2014;20(12):1983–92.

Gu Z, Eils R, Schlesner M. Complex heatmaps reveal patterns and correlations in multidimensional genomic data.. Bioinformatics 2016;32(18):2847–9.!

van der Maaten L, Hinton G. Visualizing Data using t-SNE. 2008:!

Bates D, Mächler M, Bolker B, Walker S. Fitting Linear Mixed-Effects Models Using lme4. J Stat Softw 2015;67(1). doi:10.18637/jss.v067.i01!

Pérez-Enciso M, Tenenhaus M. Prediction of clinical outcome with microarray data: a partial least squares discriminant analysis (PLS-DA) approach.. Hum Genet 2003;112(5–6):581–92.


# INCOMMON: the model

A hierarchical Bayesian generative model that infers, for each mutation in a tumour sample, the total copy number at the locus and the number of copies carrying the mutation.

## Observation model
For mutation i with total reads d_i and mutant reads r_i:

- d_i ~ Poisson(λ_i), λ_i = η[2(1 − π) + π k_i]
- r_i | d_i ~ Binomial(d_i, φ_i), φ_i = π m_i / [2(1 − π) + π k_i]

Unknowns: purity π and reads per copy η (shared across the sample); total copy number k_i and mutation multiplicity m_i (integers, 1 ≤ m_i ≤ k_i ≤ 8). Normal cells contribute two copies, tumour cells k_i; the Poisson depth followed by a binomial split induces overdispersion without an extra parameter. All mutations in a sample are modelled jointly. (Results, equations 1 to 3; Methods, equations 5 to 8.)

## Priors
- (k, m) configurations: empirical priors from PCAWG and HMF whole genomes, gene- and tissue-specific for frequently mutated genes, kernel-smoothed where sparse.
- π: Beta prior centred on the sample purity estimate. η: Gamma prior from sequencing depth.

The priors are what make copy number identifiable from targeted panels without a matched normal.

## Inference and output
MCMC gives the joint posterior; π and η are marginalised. Dosage is summarised as FAM = E[m/k | data], the posterior mean fraction of alleles carrying the mutation (equation 4; Methods equation 16). Posterior predictive checks assess fit.

## Downstream clinical analysis
FAM is cut into low, balanced and high dosage classes (tumour suppressors 0.25/0.75, oncogenes 0.33/0.66; thresholds found by maximally selected rank statistics on overall survival). The classes then enter Kaplan–Meier and multivariable Cox models (survival), logistic regression (metastatic propensity) and multinomial logistic regression (organotropism).

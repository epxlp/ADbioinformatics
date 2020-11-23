# AD Bioinformatics tutorial

#### In this session we will use some online tools to investigate possible functional mechanisms of AD GWAS loci

#### As you go through this tutorial, remember our 4 key questions:

#### - What is the causal variant?
#### - What is the causal gene?
#### - Which cell type is affected?
#### - What is the mechanism/pathway that is disturbed?



## GWAS association results

1. Download the file rs112111458_region_results.txt from this github repository to your computer

2. First open the file in excel and take a look at the results included. Sort the sheet to find the strongest association.

> Q. What is the rsid of the lead SNP?

3. We won't use a formal fine-mapping method in this practical, but you could create a reasonable credible set by identifying all variants with p<0.01

4. Enter the region containing the p<0.01 SNPs into the ensembl genome browser. NB - results use GR37 - so be sure to use the right browser version.

> Q. Is the causal variant likely to be coding or regulatory?




## GTEx - eQTL analysis

5. Go to the GTEx website www.gtexportal.org and enter the lead SNP rsid into the 'single-tissue eQTLs' search.

> Q. Which gene is the lead SNP associated with the expression of?

> Q. In which tissues is this observation seen?

> Q. Is the AD-risk allele associated with increased or decreased expression?

6. Go back to the home page and enter the gene name into the 'gene ID' search.

> Q. Is the gene specifically or ubiquitously expressed?





## Haploreg

7. Go to the Haploreg website https://pubs.broadinstitute.org/mammals/haploreg/haploreg.php and enter the lead SNP rsid. Click run. Have a look at the output.
Haploreg by default will include all SNPs with an LD r2>0.8. Alter this on the options page to include all SNPs with r2>0.4 with the lead SNP (NB - this is an arbitrary selection to give you a nice amount of output - it's probably too liberal in reality)

> Q. What annotations from haploreg might be important?

> Q. Can you tell from Haploreg which variant might be the causal variant?

> Q. Can you tell from Haploreg which gene might be the causal gene? 

> Q. Why might the results be different to GTEx?

8. Before moving on. Copy this new list of SNPs - we'll use it in the next section. (It might help to copy the whole table to a spreadsheet)





## RegulomeDB

9. Go to regulomedb.org and enter the list of SNPs from Haploreg (or the list that have p<0.01).
10. Click the '?' in the score colum to find out what the score represents.Go down the help page to find out what data the score is combining
11. Now go back to the list of scores for the SNP you entered. You can click on the scores to get more information about the underlying data

> Q. Which SNP(s) has/have the lowest score?

> Q. How confident would you be that you have identified the causal variant?

> Q. Can you tell from regulomeDB which gene might be the causal gene?

> Q. Why might the results be different to GTEx and Haploreg?





## FUMA

Go to the FUMA website fuma.ctglab.nl

12. Register for an account

13. Then go the the SNP2GENE page and edit the job instructions as follows:
- In section 1, use the file rs112111458_region_results.txt and enter the relevant column names
- In section 2, name the sample size column and change the minimum p-value to 1e-5
- In section 3-2, select to perform eQTL mapping and select 'all' tissue types.
- In section 3-3, select to perform chromatin interaction mapping, using 'all' tissue types and annotate promoters/enhancers using 'all' tissue types
- In section 5, select to perform MAGMA with 'GTEx v8 54 tissues'
- Now give your job a useful name and hit run
- Results should be returned after a few minutes

14. Navigate through the results pages. See what you can discover and how they visualise some of the results.

> Q. Do you get the same information as you got from the separate tools above?

> Q. Do you get extra information?

> Q. Do you find the presentation of results useful?




## The Open Targets Genetics platform

15. Navigate to genetics.opentargets.org

16. Enter the lead SNP

> Q. What gene(s) does the platform predict for the function of this SNP?

> Q. What are the limitations of this platform?




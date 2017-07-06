 
## SNPair_LD

Measure pair-wise linkage disequilibrium from a VCF file. The linkage disequilibrium metrics D' and R^2 are calculated for each SNP pair in a VCF file, and statistical significance is assessed. To compensate for the large number of pairwise comparisons, p-values are FDR corrected. 

## Requirements

SNPair_LD.R requires the following libraries:

- pegas
- fields
- genetics
- reshape2
- ggplot2

## Usage

```
SNPair_LD.R <vcf_file> <output_prefix>
```

A complete run of `SNPair_LD.R` will produce the following output files:

- `<prefix>_Dc.pdf`: Heatmap with all pairwise D' values
- `<prefix>_R2.pdf`: Heatmap with all pairwise R^2 values
- `<prefix>_Dc_sig.pdf`: Heatmap with the pairwise D' values of the statistically significant pairs
- `<prefix>_R2_sig.pdf`: Heatmap with the pairwise R^2 values of the statistically significant pairs
- `<prefix>_Dc_hist.pdf`: Histogram with the distribution of D' values
- `<prefix>_R2_hist.pdf`: Histogram with the distribution of R^2 values
- `<prefix>_pval.pdf`: Heatmap with the pairwise LD p-values.
- `<prefix>_qval.pdf`: Heatmap with the FDR corrected pairwise LD p-values.
- `<prefix>.log`: Text file with summary information about the LD results
- Significant_snp_pairs.csv: Tabular file with a list of the statistically significant SNP pairs.

## Output examples

#### Heatmap of pairwise D' for all SNPs

<img src="https://github.com/ODiogoSilva/SNPair_LD/raw/master/examples/teste_Dc.png">

#### Heatmap of pairwise D' for statistically significant SNP pairs

<img src="https://github.com/ODiogoSilva/SNPair_LD/raw/master/examples/teste_Dc_sig.png">

#### Distribution of pairwise D' values

<img src="https://github.com/ODiogoSilva/SNPair_LD/raw/master/examples/teste_Dc_hist.png">
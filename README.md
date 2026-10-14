# Lysosomal Enzyme Analysis: IDS

## Enzyme Information
- **Enzyme name:** Iduronate 2-sulfatase (alpha-L-iduronate sulfate sulfatase)
- **Gene symbol:** IDS
- **NCBI protein record:** [NP_000193.1](https://www.ncbi.nlm.nih.gov/protein/NP_000193.1) (isoform a preproprotein, *Homo sapiens*)
- **Function:** IDS is a lysosomal sulfatase that removes the 2-O-sulfate group from iduronic acid residues of the glycosaminoglycans heparan sulfate and dermatan sulfate. This step is required before other lysosomal enzymes can continue degrading these molecules, so IDS keeps glycosaminoglycans from building up inside lysosomes.

## Figures

### Figure 1: Amino acid composition
![Amino acid composition of IDS](figures/IDS_amino_acid_composition.png)

### Figure 2: Potential N-glycosylation motifs
![Potential N-glycosylation motifs in IDS](figures/IDS_potential_N_glycosylation.png)

## Questions

**1. What does your enzyme normally break down inside lysosomes?**

IDS helps break down the glycosaminoglycans (GAGs) heparan sulfate and dermatan sulfate. It specifically removes the sulfate group attached to iduronic acid residues in these chains, which allows other lysosomal enzymes to degrade them further into small products the cell can recycle.

**2. What is the total length of your protein, and which amino acids are most common?**

The IDS protein (NP_000193.1) is **550 amino acids** long. The five most common amino acids are:

| Rank | Amino acid | Count | Percent |
|---|---|---|---|
| 1 | Leucine (L) | 61 | 11.09% |
| 2 | Proline (P) | 52 | 9.45% |
| 3 | Serine (S) | 45 | 8.18% |
| 4 | Aspartate (D) | 39 | 7.09% |
| 5 | Valine (V) | 34 | 6.18% |

**3. How many potential N-glycosylation motifs did you find? Where are they located?**

I found **8** potential N-glycosylation motifs (N-X-S/T, where X is not proline). Their positions along the protein are:

| Position | Motif |
|---|---|
| 31 | NST |
| 115 | NFS |
| 144 | NHT |
| 246 | NIT |
| 280 | NIS |
| 325 | NST |
| 513 | NFS |
| 537 | NDS |

The motifs are spread across the whole protein, with two near the N-terminus (31 and 115), a cluster in the middle (144 to 325), and two near the C-terminus (513 and 537).

**4. Why can glycosylation matter for lysosomal proteins? Does finding a motif prove the protein is glycosylated?**

Many lysosomal enzymes are made in the endoplasmic reticulum, where N-glycans are attached to asparagine residues. In the Golgi, some of these glycans receive a mannose-6-phosphate (M6P) tag. M6P receptors recognize this tag and sort the enzyme to the lysosome instead of letting it be secreted. Glycosylation also helps with correct folding, stability, and protection from degradation.

**No, finding a motif does not prove glycosylation.** N-X-S/T only shows that a site is *possible* based on the amino acid sequence. It does not confirm that a glycan is attached, that the site is actually used, or that an M6P tag is present. Not every motif is occupied in the cell, and sequence analysis does not directly measure enzyme activity. Experimental evidence (such as mass spectrometry) is needed to confirm glycosylation.

**5. What could happen in the cell if your enzyme did not work properly?**

If IDS is missing or not working, heparan sulfate and dermatan sulfate cannot be fully degraded and accumulate inside lysosomes. The lysosomes swell and cell function is disrupted. In humans, loss of IDS function causes **mucopolysaccharidosis type II (MPS II, Hunter syndrome)**, an X-linked lysosomal storage disease. It affects multiple tissues and can involve skeletal abnormalities, enlarged organs, breathing and heart problems, and, in severe forms, effects on the brain.

## Files in this repository
- `lysosomal_enzyme_analysis.R`: R script used for the analysis
- `data/IDS.fasta`: protein sequence downloaded from NCBI
- `results/`: summary, amino acid counts, and motif position tables (CSV)
- `figures/`: Figure 1 and Figure 2

## Note
N-X-S/T is a potential N-glycosylation motif, not confirmation of a glycan or a mannose-6-phosphate tag. Protein sequence analysis does not directly measure enzyme activity.
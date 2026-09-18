Gene Mutation to Disease:

Computational Analysis of the PAH c.1222C>T (p.Arg408Trp) Variant in Phenylketonuria

Name: Kyla Rose D. Villegas
Course: BIO 300 – Cell & Molecular Biology
Section: B
Instructor: Ma’am Lilibeth Bucol
Date: September 18, 2026

I. Disease Background

Phenylketonuria (PKU) is an inherited metabolic disorder caused primarily by pathogenic variants in the PAH gene, which encodes the enzyme phenylalanine hydroxylase. The disorder follows an autosomal recessive inheritance pattern, meaning that an affected individual usually inherits one pathogenic PAH allele from each parent. Phenylalanine hydroxylase normally catalyzes the conversion of the amino acid phenylalanine into tyrosine, using tetrahydrobiopterin (BH4) as a cofactor. When PAH enzyme activity is reduced or absent, phenylalanine cannot be metabolized efficiently and accumulates in the blood and other tissues, producing hyperphenylalaninemia. Persistently elevated phenylalanine concentrations are particularly harmful to the developing nervous system because they can interfere with normal brain development and neurological function. If untreated, PKU may result in intellectual disability, developmental delay, seizures, behavioral or psychiatric abnormalities, movement problems, eczema, decreased pigmentation of the skin and hair, and a characteristic musty body odor. Early detection through newborn screening and proper control of phenylalanine levels can greatly reduce the risk of severe neurological complications. Thus, PKU demonstrates how a change in a single gene can disrupt an important metabolic pathway and produce systemic and neurological consequences (Arnold & Vockley, 2025; National Library of Medicine, n.d.).

II. Gene and Normal Protein Function

The PAH gene, which stands for phenylalanine hydroxylase, is located on chromosome 12 at 12q23.2. It encodes the enzyme phenylalanine hydroxylase, also known as phenylalanine-4-hydroxylase, which belongs to the biopterin-dependent aromatic amino acid hydroxylase family. The normal function of this enzyme is to catalyze the conversion of L-phenylalanine to L-tyrosine, using tetrahydrobiopterin (BH4) as a cofactor. This reaction is the rate-limiting step in phenylalanine catabolism and helps prevent excessive accumulation of phenylalanine in the body. Phenylalanine hydroxylase is primarily located in the cytosol and participates in phenylalanine catabolism, aromatic amino acid metabolism, and L-tyrosine biosynthesis (National Center for Biotechnology Information [NCBI], 2026; UniProt Consortium, 2026).

III. Documented Mutation

Table 1. Documented PAH c.1222C>T (p.Arg408Trp) Variant Associated with Phenylketonuria (PKU)

Parameter

Information

Gene

PAH

Reference transcript

NM_000277.3

Exact variant notation

NM_000277.3.1222C>T

Nucleotide change

C → T at coding nucleotide 1222

Predicted protein change

NP_000268.1.Arg408Trp (R408W)

Mutation type

Missense single-nucleotide variant (SNV)

Codon change

CGG → TGG

ClinVar Variation ID

577

ClinVar condition accession

RCV000000607.79

Clinical interpretation

Pathogenic

Associated disease

Phenylketonuria (PKU)

Note. Variant information was obtained from NCBI ClinVar (Variation ID 577; condition accession RCV000000607.79).

IV. Hypothesis

The documented PAH NM_000277.3.1222C>T mutation was hypothesized to produce a missense single-nucleotide substitution in which cytosine (C) is replaced by thymine (T) at coding nucleotide position 1222. Because the mutation is a substitution rather than an insertion or deletion, the reading frame was expected to remain unchanged, and the predicted protein was expected to retain its normal length of 452 amino acids. However, the resulting p.Arg408Trp (R408W) amino-acid substitution was predicted to impair phenylalanine hydroxylase activity, thereby decreasing the normal conversion of phenylalanine to tyrosine.

V. Methods

A stepwise computational workflow was performed using NCBI RefSeq for sequence retrieval and Galaxy for translation and protein-sequence comparison. The original wild-type sequence was preserved throughout the analysis, and all mutations were introduced only into separate copies, as required by the laboratory procedure.

1. Retrieval of the PAH reference sequence

The human PAH reference transcript NM_000277.3 was obtained from NCBI RefSeq. The coding sequence corresponding to nucleotides 115–1473 was used, giving a CDS length of 1,359 nucleotides. The corresponding reference protein accession was NP_000268.1. The WT coding sequence was saved in FASTA format as PAH_WT_CDS.fasta.

2. Creation of the Galaxy history and upload of the WT CDS

A new Galaxy history was created and named Villegas_Phenylketonuria_PAH_Mutation_Lab. The file PAH_WT_CDS.fasta was uploaded into this history and used as the wild-type control.

3. Translation of the wild-type PAH CDS

The WT CDS was translated using EMBOSS Transeq in Galaxy. The input sequence was PAH_WT_CDS.fasta. The translation settings were set to Frame 1 (+1) using the Standard genetic code. The options to trim the sequence and remove stop characters were left disabled so that the terminal stop symbol could be retained in the output. The translated sequence was saved as PAH_WT_protein.fasta. The resulting predicted protein contained 452 amino acids, began with MSTAVLENPG, ended with ILCSALQKIK, and contained a terminal * representing the stop codon. These results were checked against the reference protein NP_000268.1.

4. Creation of the documented PAH mutant CDS

A copy of the WT CDS was made so that the original reference sequence remained unchanged. The documented variant NM_000277.3.1222C>T was then reproduced manually by changing the nucleotide at CDS position 1222 from cytosine (C) to thymine (T). This changed the codon from CGG to TGG, corresponding to the predicted amino-acid substitution p.Arg408Trp (R408W). No nucleotides were inserted or deleted. The mutant sequence was saved as PAH_c1222C_T_CDS.fasta.

5. Translation of the documented mutant sequence

The file PAH_c1222C_T_CDS.fasta was uploaded to the same Galaxy history and translated using EMBOSS Transeq with exactly the same settings used for the WT sequence: Frame 1 (+1), Standard genetic code, with trimming and sequence cleaning disabled. The translated mutant protein was saved as PAH_R408W_protein.fasta. The mutant CDS remained 1,359 nucleotides, and the predicted mutant protein remained 452 amino acids long. The first amino-acid difference occurred at position 408, where arginine (R) in the WT sequence was replaced by tryptophan (W). No premature stop codon or reading-frame change was observed.

6. Pairwise comparison of WT and R408W proteins

The wild-type and documented mutant predicted protein sequences were compared using EMBOSS Needle in Galaxy. The WT protein PAH_WT_protein.fasta was entered as the first sequence, and PAH_R408W_protein.fasta was entered as the second sequence. The alignment used the EBLOSUM62 substitution matrix, a gap-opening penalty of 10.0, and a gap-extension penalty of 0.5. The brief alignment option was enabled. The resulting pairwise alignment was saved as PAH_WT_vs_R408W_alignment.txt. The alignment showed 452/453 identical aligned positions (99.8%), 452/453 similar aligned positions (99.8%), and 0/453 gaps (0.0%), with the only amino-acid difference occurring at residue 408, where arginine (R) in the WT sequence was replaced by tryptophan (W).

7. Creation of the artificial mutation

For the second controlled experiment, another independent copy of the WT CDS was created. A single-nucleotide substitution, PAH c.21A>G, was introduced by changing adenine (A) to guanine (G) at CDS position 21. This changed the codon from GAA to GAG. Because both codons encode glutamic acid, the mutation was predicted to be synonymous. The artificial mutant CDS was saved as PAH_artificial_c21A_G_CDS.fasta.

8. Translation of the artificial mutant

The artificial mutant CDS was translated in Galaxy using EMBOSS Transeq with the same settings used for both the WT and documented mutant sequences: Frame 1 (+1) and the Standard genetic code, with trimming and cleaning disabled. The resulting predicted protein was saved as PAH_artificial_c21A_G_protein.fasta. The protein remained 452 amino acids long, and its predicted amino-acid sequence was identical to the WT protein, confirming that c.21A>G was synonymous.

VI. Results

The computational analysis of the wild-type, documented mutant, and artificial mutant PAH sequences showed that all three coding sequences remained 1,359 nucleotides long and produced predicted proteins of 452 amino acids. The documented c.1222C>T mutation caused a single amino-acid substitution at residue 408, whereas the artificial c.21A>G mutation did not alter the predicted amino-acid sequence.

Table 2. Wild-Type PAH Translation Results

Parameter

Result

Dataset used

PAH_WT_CDS.fasta

CDS length

1,359 nt

Reading frame

Frame 1 (+1)

Start codon

ATG

Stop codon

TAA

Predicted protein length

452 amino acids

First 10 amino acids

MSTAVLENPG

Last 10 amino acids

ILCSALQKIK

Translation stop symbol

*

Predicted protein filename

PAH_WT_protein.fasta

Table 3. Translation Results of the Documented PAH c.1222C>T (p.Arg408Trp) Mutant

Parameter

Result

Mutant CDS filename

PAH_c1222C_T_CDS.fasta

Mutant CDS length

1,359 nt

Mutant protein filename

PAH_R408W_protein.fasta

Predicted protein length

452 amino acids

Reading frame

Frame +1

First amino-acid difference

Position 408

WT amino acid at position 408

Arginine (R)

Mutant amino acid at position 408

Tryptophan (W)

Premature stop codon

Absent

Approximate amino acids affected

1 amino acid

Table 4. Overall Comparison of Wild-Type, Documented, and Artificial PAH Variants

Parameter

WT PAH

Documented c.1222C>T

Artificial c.21A>G

CDS length

1,359 nt

1,359 nt

1,359 nt

Protein length

452 aa

452 aa

452 aa

Mutation type

None / WT

Missense substitution

Synonymous substitution

Codon change

None

CGG → TGG

GAA → GAG

Reading frame changed

No

No

No

Premature stop codon

No

No

No

Amino acids affected

None

Arg408Trp

None

Protein sequence changed

No

Yes, at residue 408

No

VII. WT versus Mutant Protein Comparison

The predicted wild-type PAH protein and the documented R408W mutant protein were compared using EMBOSS Needle. Both proteins were 452 amino acids long, and the alignment showed that they differed at only one amino-acid position. At residue 408, the wild-type protein contained arginine (R), whereas the mutant contained tryptophan (W). No amino acids were inserted or deleted, no downstream amino acids were altered, and no premature stop codon was produced. The reading frame also remained unchanged. The alignment showed 452/453 identical aligned positions (99.8%) with 0/453 gaps, confirming that the documented c.1222C>T variant produced a single missense substitution rather than a frameshift or truncation.

Table 5. Comparison of the Wild-Type and PAH R408W Predicted Protein Sequences

Parameter

Wild-Type PAH

R408W Mutant

Protein length

452 aa

452 aa

Residue at position 408

Arginine (R)

Tryptophan (W)

First sequence difference

—

Position 408

Amino acids affected

None

1 amino acid

Downstream amino acids changed

No

No

Insertion/deletion

None

None

Premature stop codon

No

No

Reading frame changed

No

No

Sequence identity

—

452/453 (99.8%)

Gaps in alignment

—

0/453 (0.0%)

Mutation type

Wild type

Missense substitution

VIII. Artificial Mutation Experiment

A second controlled mutation was introduced into a separate copy of the wild-type PAH coding sequence to determine how a different single-nucleotide substitution could affect the predicted protein. The artificial mutation selected was PAH c.21A>G, in which adenine (A) at coding nucleotide position 21 was replaced by guanine (G). This changed the codon from GAA to GAG. Because both codons encode glutamic acid (E), the mutation was predicted to be synonymous. After translation in Galaxy using the same EMBOSS Transeq settings applied to the WT and documented mutant sequences, the artificial mutant still produced a predicted protein of 452 amino acids. No reading-frame change, premature stop codon, or amino-acid substitution was observed. The predicted protein sequence remained identical to the wild-type sequence, confirming that the c.21A>G substitution did not alter the encoded amino-acid sequence.

Table 6. Results of the Artificial PAH c.21A>G Synonymous Mutation Experiment

Parameter

Result

Artificial mutation

PAH c.21A>G

Nucleotide change

A → G at CDS position 21

Original codon

GAA

Mutant codon

GAG

Mutation type

Synonymous single-nucleotide substitution

Amino acid before mutation

Glutamic acid (E)

Amino acid after mutation

Glutamic acid (E)

CDS length

1,359 nt

Predicted protein length

452 aa

Reading frame changed

No

Premature stop codon

No

Protein sequence changed

No

Predicted direct effect on protein sequence

None

IX. Molecular Interpretation: Gene → Mutation → Protein → Cellular Effect → Phenotype

The PAH gene encodes phenylalanine hydroxylase, an enzyme that normally converts phenylalanine to tyrosine. In the documented variant NM_000277.3.1222C>T, cytosine (C) at coding nucleotide position 1222 is replaced by thymine (T), changing the codon from CGG to TGG. This codon change replaces arginine with tryptophan at amino-acid position 408, producing the missense variant p.Arg408Trp (R408W). The computational analysis showed that the mutation did not alter the reading frame or overall protein length; both the WT and mutant predicted proteins remained 452 amino acids long, with only one amino-acid difference at residue 408 and no premature stop codon.

Although the computational analysis establishes the sequence-level consequence of the mutation, its effects on actual protein behavior require experimental evidence. Published evidence indicates that the R408W substitution can reduce PAH structural stability and enzymatic activity (Arnold & Vockley, 2025). Reduced functional PAH decreases the normal conversion of phenylalanine to tyrosine, allowing phenylalanine to accumulate in the blood and tissues. Persistently elevated phenylalanine can interfere with normal neurological development and function, producing the clinical manifestations of phenylketonuria (PKU).

Table 7. Molecular Interpretation of the PAH c.1222C>T Mutation Leading to Phenylketonuria

Level

Molecular consequence

Gene

PAH encodes phenylalanine hydroxylase

Mutation

NM_000277.3.1222C>T

DNA change

C → T at coding nucleotide 1222

Codon change

CGG → TGG

Protein change

p.Arg408Trp (R408W)

Protein-level result

One amino-acid substitution; protein remains 452 aa

Reading frame

Unchanged

Premature stop codon

None

Expected functional effect

Reduced PAH stability and enzymatic activity based on published evidence

Cellular/biochemical effect

Reduced conversion of phenylalanine to tyrosine and increased phenylalanine accumulation

Phenotype

Phenylketonuria (PKU), particularly neurological effects associated with elevated phenylalanine

X. Limitations

This study was limited to computational sequence analysis and did not include laboratory experiments to directly measure PAH protein expression, folding, stability, cellular localization, or enzymatic activity. The Galaxy workflow could determine the predicted effects of the PAH c.1222C>T mutation on the coding and amino-acid sequences, but it could not demonstrate how the R408W protein actually behaves inside human cells. Therefore, conclusions regarding reduced PAH activity, phenylalanine accumulation, and the development of phenylketonuria depended on evidence from published experimental and clinical studies. The analysis was also limited to one documented pathogenic variant and one artificial synonymous mutation, so the results do not represent the effects of all possible PAH variants. Additional biochemical, structural, cellular, and clinical studies would be needed to fully determine the functional consequences of the mutation.

XI. Conclusion

This computational analysis demonstrated how a single nucleotide change in the PAH gene can alter the predicted protein sequence and contribute to the molecular basis of phenylketonuria. The documented PAH c.1222C>T variant changed the codon from CGG to TGG, resulting in the missense substitution p.Arg408Trp (R408W). Despite this amino-acid change, the reading frame remained unchanged, no premature stop codon was introduced, and both the wild-type and mutant predicted proteins remained 452 amino acids long. In contrast, the artificial c.21A>G substitution changed the codon from GAA to GAG but did not alter the encoded amino acid, demonstrating a synonymous mutation. Overall, the results show that different single-nucleotide substitutions can produce different molecular consequences depending on how they affect the genetic code. The computational findings support the sequence-level effect of the R408W variant, while its effects on PAH stability, enzymatic activity, phenylalanine metabolism, and the development of PKU require support from published experimental and clinical evidence.

Project Links

Galaxy history:
https://galaxy-main.usegalaxy.org/u/kylarosevillegas/h/villegas-phenylketonuria-pah-mutation-lab

GitHub repository:
https://github.com/kylarosevillegas/Phenylketonuria-PAH-Mutation-Lab

XII. References

Arnold, G., & Vockley, J. (2025). Phenylalanine hydroxylase deficiency. In M. P. Adam, S. Bick, G. M. Mirzaa, et al. (Eds.), GeneReviews®. University of Washington, Seattle.
https://www.ncbi.nlm.nih.gov/books/NBK1504/

National Center for Biotechnology Information. (2026). NM_000277.3(PAH).1222C>T (p.Arg408Trp). ClinVar.
https://www.ncbi.nlm.nih.gov/clinvar/variation/577/

National Center for Biotechnology Information. (2026). NM_000277.3(PAH).1222C>T (p.Arg408Trp) and phenylketonuria. ClinVar.
https://www.ncbi.nlm.nih.gov/clinvar/RCV000000607/

National Center for Biotechnology Information. (2026). PAH phenylalanine hydroxylase [Homo sapiens (human)]. NCBI Gene.
https://www.ncbi.nlm.nih.gov/gene/5053

National Library of Medicine. (n.d.). Phenylketonuria. MedlinePlus Genetics.
https://medlineplus.gov/genetics/condition/phenylketonuria/

UniProt Consortium. (2026). Phenylalanine-4-hydroxylase (PAH) – Homo sapiens. UniProtKB (P00439).
https://www.uniprot.org/uniprotkb/P00439/entry

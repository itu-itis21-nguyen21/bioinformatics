# BLG348E Introduction to Bioinformatics term project

In this term project, we ran 12 variant calling pipelines on a pair of healthy and cancerous genomes using a comprehensive pipeline creation tool called COSAP (https://github.com/MBaysanLab/cosap). Each variant calling pipeline follows the following procedure:
- Importing FASTQ files
- Trimming
- Mapping: either Bowtie2 or BWA
- Duplicate removal
- Base recalibration: either included or not
- Variant calling: either Somatic Sniper, Strelka2, or Mutect2

We then analyzed and compared the variant set that each pipeline returns, using visualization tools (graphs, heatmaps, PCA) and statistical techniques (precision, recall, F1-score). The report contains a complete treatment of the results, analysis, and discussion. Interested readers can learn more about the project or access input data in the project description file.

**Key takeaways:**
- Most variations in outputs, precision, recall, and F1 score can be attributed to variant calling algorithms. Among the three algorithms, Mutect2 has the best performance.
- The choice of mappers and base recalibration affects precision and recall to a certain extent.
- There is a precision-recall tradeoff concerning the number of variant outputs.
- Over half of gold-standard variants are detected by all 12 pipelines. However, 15% of gold-standard variants get detected by no pipelines.
- Higher read depth has a positive impact on detection accuracy. Nevertheless, exceptionally high read depth appears to be associated with false positives.

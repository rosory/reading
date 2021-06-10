# 读文献

1. ctDNA

   1.1 [Bioinformatics Analysis for Cell-Free Tumor DNA Sequencing Data](./references/chen2018.pdf)

```Mermaid
graph TD
    A("Raw data(BCL format files)") --> |"de-multiplexing<--bcl2fastq"| B(FASTQ files);
    %% style A fill:#63CA01,stroke:#333;
    B -->|"FASTQ QC<--FastQC"| C(FASTQ QC report);
    B -->|data preprocessing| D(filtered fastq);
    D -->|alignment<--BWA| E(original BAM);
    E -->|BAM sorting| F(sorted BAM);
    F --> G(BAM QC report);
    F -->|realignment deduplication| H(final BAM);
    H -->|Variant calling| I(original VCF);
    I -->|database annotation| J(database annotated VCF);
    J -->|baseline annotation| k(baseline annotated VCF);
    k -->|unique read counting| L(Complete VCF);
    L -->|variant filtering| M(clean variants);
    L -->|visualization| N(Visualized targets);
    N -->|interactive analysis| o(clinical interpretation)
```


# 读文献

1. ctDNA

   1.1 [Bioinformatics Analysis for Cell-Free Tumor DNA Sequencing Data](./references/chen2018.pdf)

```Mermaid
graph TD
    A(Raw data) --> |de-multiplexing| B(FASTQ files);
    %% style A fill:#63CA01,stroke:#333;
    B -->|FASTQ QC| C(FASTQ QC report);
    B -->|data preprocessing| D(filtered fastq);
    D -->|alignment| E(original BAM);
    E -->|BAM sorting| F(sorted BAM);
    F --> G(BAM QC report);
    F -->|realignment deduplication| H(final BAM);
    H -->|Variant calling| I(original VCF)
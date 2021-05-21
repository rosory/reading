# 读文献

1. ctDNA

   1.1 [Bioinformatics Analysis for Cell-Free Tumor DNA Sequencing Data](./references/chen2018.pdf)

```Mermaid
graph TD
    A(Raw data) --> |de-multiplexing| B(FASTQ files);
    %% style A fill:#63CA01,stroke:#333;
    B -->|Yes| C[OK];
    C --> D[Rethink];
    D --> B;
    B ---->|No| E[End];   
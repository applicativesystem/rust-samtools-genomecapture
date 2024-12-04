# rust-samtools-genomecapture

- rust samtools genomecapture.
- give the id list, reference genome, upstream and downstream and extracts the reference genome portion for the genome browser. 
-  rust-samtools-genome-capture: takes a genome alignment files, a reference fasta file, the upstream and the downstream regions and the path to the prank aligner and then
 aligns the extracted regions and also outputs a unaligned file.
- targetd capture assay development for taking reads from HybSeq.
- general note: Incase of Golang and RUST, please see the last commit message and if it says compiled binary then it is completed or else still in development version.


```
cargo build 

```
```
λ gauravsablok rust-samtools-genomecapture → λ git main* → ./target/debug/rust-samtools-genome-capture -h
Usage: rust-samtools-genome-capture <ALIGNMENT_ARG> <IDLIST_ARG> <FASTA_ARG> <UPSTREAM_ARG> <DOWNSTREAM_ARG> <READLENGTH_ARG>

Arguments:
  <ALIGNMENT_ARG>   please provide the path to the alignment file
  <IDLIST_ARG>      please provide the id list for the specific region
  <FASTA_ARG>       please provide the fasta file used for the reference alignment
  <UPSTREAM_ARG>    please provide the upstream add from the sam alignments to be extracted
  <DOWNSTREAM_ARG>  please provide the downstream add from the sam alignments to be extracted
  <READLENGTH_ARG>  please provide the readlength of the sequencing reads

Options:
  -h, --help     Print help
  -V, --version  Print version
```


- how to run the binary

```
/target/debug/rust-samtools-genome-capture ./sample-files/alignreads-metagenomics.sam \
                           ./sample-files/sample-list.txt ./sample-files/sample-ids.fasta 10 10

``
- result from the rust-samtools-genome-capture

```
- selected-ids-downstream.fasta - downstream for those ids 
- selected-ids-reads.fasta - reads aligned to those ids.
- selected-ids-upstream.fasta - upstreams for those ids.
- selected-ids-upstream-region-downstream.fasta - upstream-region -downstream for those ids.

```
Gaurav Sablok

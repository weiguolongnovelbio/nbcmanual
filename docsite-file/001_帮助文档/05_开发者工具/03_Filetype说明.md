###  **FileType简单说明**
　　在task链接时,下游task的输入文件有固定的类型.每种类型对应的文件后缀名有固定的格式要求,如不满足要求,则不允许选择。
<div style="text-align:center"><img data-src="1.png" width="550px" ></img>
</div>

我们定义一个文件后缀由Suffix、Extension、ZipExtension三部分组成，类似：
prefix.Suffix.Extension.ZipExtension
其中：
Suffix为文件末尾，后缀名之前的字段；
Extension为后缀名；
ZipExtension为压缩格式。

譬如我们有个文件为 mycontrol.1.fastq.gz 那么在这里Suffix为1，Extension为fastq，ZipExtension为gz。

下表展示了不同文件类型要求的文件名样式。NAN表示为空, ANY表示任意(包括为空)。

| FileType       | Suffix   |  Extension  | ZipExtension  | example |
| --------  |: -----: | :----:  |:----:  |:----:  |
| SAM     | ANY   |  sam    | NAN | `*.sam`  |
| BAM        |   ANY   |   bam  | NAN  |` *.bam`  |
| SORTED_BAM        |    sorted    |  bam  | NAN  |` *.sorted.bam` |
|UNMAPPED_BAM        |   unmapped   |  bam  | NAN  | `*.unmapped.bam` |
| BED	      |    ANY     |bed | NAN;gz  | `*.bed`，`*.bed.gz`	 |
| #WIG       |   ANY   |  wig  | NAN  |  	 |
| SORTED_BAM        |    sorted    |  bam  | NAN  |` *.sorted.bam`|
|BLASTFILE|ANY|blast|NAN;gz|`*.blast`,`*.blast.gz`|
|FASTA|ANY|fa;fasta|NAN|`*.fa`,`*.fasta`|
|FASTQ|ANY|fq;fastq;fq|NAN;gz|`*.fq`,`*.fasta`,`*.fq.gz`,`*.fastq.gz`|
|LEFT_FASTQ|1|fq;fastq|NAN;gz|`*.1.fq`,`*.1.fasta`,`*.1.fq.gz`,`*.1.fastq.gz`|
|RIGTH_FASTQ|2|fq;fastq|NAN;gz|`*.2.fq`,`*.2.fasta`,`*.2.fq.gz`,`*.2.fastq.gz`|
|FASTQINTERLEVE　|Interleaved　|fq;fastq　|NAN;bz2;lzo|　`*.Interleaved.fq`,`*.Interleaved.fastq`,`*.Interleaved.fq.bz2`,`*.Interleaved.fastq.bz2`,`*.Interleaved.fq.lzo`,`*.Interleaved.fastq.lzo`|
|GENETABLE|exp;diff;alldiff|txt;xls;xlsx|NAN|`*.exp.txt`,`*.diff.txt`,`*.alldiff.txt`,`*.exp.xls`,`*.exp.xlsx`,这个比较多,简单列了几个|
|GENEXPTABLE|exp;RPKM|txt;xls;xlsx|NAN|`*.exp,txt`,`*.RPKM.txt`,`*,exp.xls`|
|GENELOCTABLE|loc|txt;xls;xlsx|NAN|`*.loc.txt`,`*.loc.xls`,`*.loc.xlsx`|
|DIFGENE|diff;alldiff|txt;xls;xlsx|NAN|`*.diff.txt`,`*.alldiff.xls`等|
|VCF|ANY|vcf|NAN|`*.cvf`|
|BCF|ANY|bcf|NAN|`*.bcf`|
|GFF3|ANY|gff;gff3|NAN;gz|`*.gff`,`*.gff3`,`*.gff.gz`,`*.gff3.gz`|
|MRD|ANY|mrd|NAN|`*.mrd`|
|PILEUP|ANY|pileup|NAN;gz|`*.pileup`,`*.pileup.gz`|
|PIC|ANY|png;jpg;jpeg|NAN|`*.png`,`*.jpg`,`*.jpeg`|



	



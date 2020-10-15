# RGMGC 

GeneSet Construction Pipeline for RMGMC Metagenome Project

Including:

(1) Gene prediction in MAGs/contigs

(2) Geneset construction

(3) Gene annotations


1. Package Required

      (1) Prodigal(v.2.6.3), https://github.com/hyattpd/Prodigal
	  
      (2) CD-HIT(v.4.8.1), http://weizhongli-lab.org/cd-hit/
	  
      (3) DIAMOND(v.0.9.22), https://github.com/bbuchfink/diamond
	  
      (4) HMMER(v.3.2.1)
	  
      (5) BLAST+
	  

2.       Gene prediction (use Yak_Cecum-3 as an example)

      prodigal -a Yak_Cecum-3.temp.orf.faa -i Yak_Cecum-3.final.contigs -f gff -o Yak_Cecum-3.gff -p meta -q -d Yak_Cecum-3.temp.orf.ffn
	  

3. Geneset construction (use Yak metagenome as examples)

      cd-hit-est -i Yak_Abomasum.all.ffn -o Yak_Abomasum.geneSet.ffn -n 9 -c 0.95 -G 0 -M 0 -d 0 -aS 0.9 -r 1 -T 80
	  
      cd-hit-est -i Yak_Cecum.all.ffn -o Yak_Cecum.geneSet.ffn -n 9 -c 0.95 -G 0 -M 0 -d 0 -aS 0.9 -r 1 -T 80
	  
      cd-hit-est -i Yak_Colon.all.ffn -o Yak_Colon.geneSet.ffn -n 9 -c 0.95 -G 0 -M 0 -d 0 -aS 0.9 -r 1 -T 80
	  
      cd-hit-est -i Yak_Duodenum.all.ffn -o Yak_Duodenum.geneSet.ffn -n 9 -c 0.95 -G 0 -M 0 -d 0 -aS 0.9 -r 1 -T 80
	  
      cd-hit-est -i Yak_Ileum.all.ffn -o Yak_Ileum.geneSet.ffn -n 9 -c 0.95 -G 0 -M 0 -d 0 -aS 0.9 -r 1 -T 80
	  
      cd-hit-est -i Yak_Jejunum.all.ffn -o Yak_Jejunum.geneSet.ffn -n 9 -c 0.95 -G 0 -M 0 -d 0 -aS 0.9 -r 1 -T 80
	  
      cd-hit-est -i Yak_Omasum.all.ffn -o Yak_Omasum.geneSet.ffn -n 9 -c 0.95 -G 0 -M 0 -d 0 -aS 0.9 -r 1 -T 80
	  
      cd-hit-est -i Yak_Rectum.all.ffn -o Yak_Rectum.geneSet.ffn -n 9 -c 0.95 -G 0 -M 0 -d 0 -aS 0.9 -r 1 -T 80
	  
      cd-hit-est -i Yak_Reticulum.all.ffn -o Yak_Reticulum.geneSet.ffn -n 9 -c 0.95 -G 0 -M 0 -d 0 -aS 0.9 -r 1 -T 80
	  
      cd-hit-est -i Yak_Rumen.all.ffn -o Yak_Rumen.geneSet.ffn -n 9 -c 0.95 -G 0 -M 0 -d 0 -aS 0.9 -r 1 -T 80
	  
      cd-hit-est -i Yak.all.ffn -o Yak.geneSet.ffn -n 9 -c 0.95 -G 0 -M 0 -d 0 -aS 0.9 -r 1 -T 80

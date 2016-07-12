##RNAex: an RNA secondary structure prediction server enhanced by high-throughput structure-probing data* Yang Wu†, Rihao Qu†, Yiming Huang†, Binbin Shi, Mengrong Liu, Yang Li and Zhi John Lu*
* April, 2016.
* RNAex server to access structure probing data
* in vivo and in vitro 
* in silico: MaxExpect, SeqFold, RNAstructure, and RNAfold
* + RNA editing, RNA modification, SNP sites

============= ========= ==============
Species        Method    Sample ============= ========= ==============
Homo sapiens   DMS-seq   K562
               PARS      trio
Arabi          DMS-seq   
Mouse          icSHAPE
               Frag-seq
               CIRS-seq   

============= ========= ==============


##A comprehensive database of high-throughput sequencing-based RNA secondary structure probing data (Structure Surfer)
* Nathan D. Berkowitz, Ian M. Silverman, Daniel M. Childress, Hilal Kazan, Li-San Wang and Brian D. Gregory
* May, 2016.
* ds/ssRNA-seq (RNaseONE ss and RNase V1 ds)
\\[ S_i = \log_2 \frac{ONE_i + 1}{V_{1j}+1}
\\]

* similar to PARS
\\[
S_i = \log_2 (\sum \frac{V_{1j}+5}{5} )- \log_2 (\sum \frac{S_{1j}+5}{5})
\\]

* DMS-seq
\\[
R_i = \frac{D_i / D_{max}}{C_i / C_{max}}
\\]
* icSHAPE
\\[
R_i = (D_i - C_i) / B
\\]


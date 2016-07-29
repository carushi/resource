RNA structure papers
======================

RNAex: an RNA secondary structure prediction server enhanced by high-throughput structure-probing data
---------------------------------------------------------------------------------------------------------


* Yang Wu, Rihao Qu, Yiming Huang, Binbin Shi, Mengrong Liu, Yang Li and Zhi John Lu*
* April, 2016.
* RNAex server to access structure probing data
* in vivo and in vitro 
* in silico: MaxExpect, SeqFold, RNAstructure, and RNAfold
* + RNA editing, RNA modification, SNP sites

============= ========= ==============
Species        Method    Sample
============= ========= ==============
Homo sapiens   DMS-seq   K562
               PARS      trio
Arabi          DMS-seq   
Mouse          icSHAPE
               Frag-seq
               CIRS-seq   

============= ========= ==============


A comprehensive database of high-throughput sequencing-based RNA secondary structure probing data (Structure Surfer)
---------------------------------------------------------------------------------------------------------------------
* Nathan D. Berkowitz, Ian M. Silverman, Daniel M. Childress, Hilal Kazan, Li-San Wang and Brian D. Gregory
* May, 2016.
* ds/ssRNA-seq (RNaseONE ss and RNase V1 ds)

.. math::

	S_i = \log_2 \frac{ONE_i + 1}{V_{1j}+1}


* similar to PARS

.. math::

	S_i = \log_2 (\sum \frac{V_{1j}+5}{5} )- \log_2 (\sum \frac{S_{1j}+5}{5})


* DMS-seq (in vivo)

.. math::

	R_i = \frac{D_i / D_{max}}{C_i / C_{max}}

* icSHAPE (in vivo)

.. math::

	R_i = (D_i - C_i) / B




The RNA structurome: transcriptome-wide structure probing with next-generation sequencing.
---------------------------------------------------------------------------------------------------------------------
* Chun Kit Kwok, Yin Tang, Sarah M. Assmann, Philip C. Bevilacqua.
* April, 2015.


======== ============== =========================== ======================== ===================================
 sample   Name             Probing method            Features                   Paper
======== ============== =========================== ======================== ===================================
in vitro PARS            RNase S1 & V1 cleavage      \-\-                    Kertesz, et al. 2010. Nature
\-\-     PARTE           RNase V1                    \-\-                    Wan, et al. 2012. Mol. cell.
\-\-     FragSeq         Nuclease P1 cleavage        \-\-                    Underwood, et al. 2010. Nat. Met.
\-\-     SHAPE           2'-hydroxyl acylation       RT stops                Lucks, et al. 2011. PNAS.
\-\-     ds/ssRNA-seq    RNase ONE & V1 cleavage     \-\-                    Li, et al. 2012. Cell reports.
\-\-     Map-Seq         DMS, CMCT, 1M7              \-\-                    Smola, et al. 2014. Protocol RNA.
\-\-     HRF-Seq         hydroxyl radicals           break acc region        Kielpinski, et al. 2014. NAR.
\-\-     ChemModSeq      2'-hydroxyl acylation       \-\-                    Hector, et al. 2014. NAR.
\-\-     RING-MaP        DMS                         mutational profiling    Homan, et al. 2014. PNAS.
\-\-     SHAPE-MaP       2M7, 1M6, NMIA              mutational profiling    Smola, et al. 2015. Nat. Prot.
in vivo  DMS-seq         DMS modification            (+DMS-AC?)              Rouskin, et al. 2014. Nature.
\-\-     Mod-seq         \-\-                        \-\-                    Talkish, et al. 2014. RNA.
\-\-     Structure-seq   \-\-                        \-\-                    Ding, et al. 2014. Nat. Prot.
\-\-     CIRS-seq        CMCT, DMS                   G and AC                Incarnato, et al. 2014. Genome Biol.
\-\-     icSHAPE         NAI-N3                      AU rich?                Spittle, et al. 2015. Nature.
======== ============== =========================== ======================== ===================================

# Complete functional mapping of NHP vaccine-elicited antibody lineages that target the fusion peptide of HIV
### Adam S. Dingens,  Julie Overbaugh, and Jesse D. Bloom
### In collaboration with the Kwong and Mascola groups at the NIH VRC

Experiments analyzed here were performed by Adam Dingens in the [Bloom lab](http://research.fhcrc.org/bloom/en.html) and [Overbaugh lab](https://research.fhcrc.org/overbaugh/en.html) in the summer of 2018.  

Here, we use mutational antigenic profiling to comprehensively map escape from macaque vaccine-elicited antibodies lineages. There are two names for each antibody; the first name is used in this analysis, and the (name in parantheses) is the final name used in the publication.

These are:
> * `106B6`, `106E6 (DFPH-a.15)`, and `110D12 (DFPH-a.01)`; clonally related mAbs from from NHP **DFPH**.
> * `DF1W203 (DF1W-a.02)` and `DF1W314 (DF1W-a.01)`;  clonally related mAbs from from NHP **DF1W**.
> * `OPV12 (0PV-b.01)` and `OPV20 (0PV-a.01)`;  mAbs from from NHP **OPV**. These are not clonal varaints but do share gene usage.
> * `17D4 (A12V163-a.01)`; from NHP **A12V163**. This Ab was elicted with only trimer (no FP-KLH) and has very limited breadth  (~3%). 

We use **BG505.T332N** mutant Env virus libraries. Importantly, these libraries are sequence matched to the immunogens, which were BG505 FP (conjugated to KLH) and BG505 SOSIP trimer (though sometimes a different trimer boost was used). The generation and characterization of the BG505 mutant virus libraires is described in detail in [Haddox, Dingens et al. eLife 2018](https://elifesciences.org/articles/34420). 

[Dingens et al. Plos Pathogens 2018](https://journals.plos.org/plospathogens/article?id=10.1371/journal.ppat.1007159) details mutational antigenic profiling of the template bnAb `N123-VRC34.01` and the murine vaccine-elicited antibodies `2712-vFP16.02`, and `2716-vFP20.01`.  [Dingens et al. Cell Host & Microbe 2017](http://dx.doi.org/10.1016/j.chom.2017.05.003) explains HIV mutational antigenic profiling in detail. 

Here, we use [dms_tools2](https://jbloomlab.github.io/dms_tools2/) to analyze the data in the Jupyter notebook [analysis_notebook.ipynb](analysis_notebook.ipynb).  This notebook processes the Illumina deep sequencing data, and then analyzes the selection in the context of the antibody. 

The barcoded subamplicon Illumina sequencing approach is described in detail [here](https://jbloomlab.github.io/dms_tools2/bcsubamp.html), and `differential selection` is described [here](https://jbloomlab.github.io/dms_tools2/diffsel.html).


## Organization
The mutational antigenic profiling analysis is performed by the iPython notebook [`analysis_notebook.ipynb`](analysis_notebook.ipynb). 

Subdirectories:

   * [`./summary_results/`](summary_results) contains the final `differential selection` data in csv format, as well as the `positive differential selection` plotted across the length of the gene. Look in this folder if you simply want the final data. Note that while the rest of this computational analysis uses earlier versions of each antibody's name (see above), the files in this subdirectory are renamed accoridng to the final published name of each antibody. For easy comparison, I also included the differential selection logoplots for the humaan infection-derived bnAb `N123-VRC34.01` and the murine vaccine-elicited antibodies `2712-vFP16.02`, and `2716-vFP20.01` from [Dingens et al. Plos Pathogens 2018](https://journals.plos.org/plospathogens/article?id=10.1371/journal.ppat.1007159); [analysis here](https://github.com/jbloomlab/MAP_Vaccine_FP_Abs). For instance, [./summary_results/DF1W-a.01-medianmutdiffsel.csv](summary_results/DF1W-a.01-medianmutdiffsel.csv) givesn the numerical results for antibody `DF1W-a.01`, and [summary_results/DF1W-a.01_diffsel.pdf](summary_results/DF1W-a.01_diffsel.pdf) shows a logo plot of these results.

   * [`./results/`](results) is generated by [`analysis_notebook.ipynb`](analysis_notebook.ipynb). It contains the `codoncounts` and `differential selection` data and raw output for all figures.
   
   * `./results/FASTQ_files/` contains the input Illumina deep sequencing data. This drectory is generated by [`analysis_notebook.ipynb`](analysis_notebook.ipynb), which downloads the sequencing files from the [Sequence Read Archive](http://www.ncbi.nlm.nih.gov/sra).

   * [`./data/`](data) contains all input data needed to run [`analysis_notebook.ipynb`](analysis_notebook.ipynb). Files are described in the iPython notebok when used. 


## Results and Conclusions
All of the results are breifly detailed in the [`analysis_notebook.ipynb`](analysis_notebook.ipynb) notebook; click on this notebook to see the results.




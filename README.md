# SONIA

SONIA is a python 2.7 software developed to infer selection pressures on features of amino acid CDR3 sequences. The inference is based on maximizing the likelihood of observing a selected data sample given a representative pre-selected sample. This method was first used in Elhanati et al (2014) to study thymic selection. For this purpose, the pre-selected sample can be generated internally using the OLGA software package, but SONIA allows it also to be supplied externally, in the same way the data sample is provided.

SONIA takes as input TCR CDR3 amino acid sequences, with or without per sequence lists of possible V and J genes suspected to be used in the recombination process for this sequence. As in Elhanati (2014), its output is selection factors for each amino acid / position / CDR3 length combinations, and also for each V and J gene choice. These selection factors can be used to calculate sequence level selection factors, or energies (log of selection factors), which indicate how more or less represented this sequence would be in the selected pool as compared to the the pre-selected pool. These in turn could be used to calculate the probability to observe any sequence after selection. A convenience class EvaluateModel is included that can load a previously inferred model and perform such tasks.

An example script is provided that reads in selected and pre-selected sequences from supplied text files and infer selection factors on any amino acid / position / CDR3 length combinations and V/J identity, saving the inferred model to a file. Then the model is loaded into the EvaluateModel to generate sequences before and after selection, and calculate probabilities and energies for the generated sequences.

## Installation

The provided `environment.yml` file describes the SONIA dependencies.

---

Free use of SONIA is granted under the terms of the GNU General Public License version 3 (GPLv3).

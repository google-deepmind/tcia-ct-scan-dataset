# TCIA Test & Validation Radiotherapy CT Planning Scan Dataset

## Usage
The dataset is stored via Git LFS. To download the full repository, first follow the [Git LFS installation instructions](https://git-lfs.github.com/) then run:

```sh
git lfs clone https://github.com/deepmind/tcia-ct-scan-dataset
```

## Summary
This dataset consists of previously open sourced head and neck scans, each segmented with full volumetric regions by trained radiographers according to standard segmentation class definition found in the atlas proposed in Brouwer et al (2015). The test and validation sets were created as part of the DeepMind-UCLH collaboration to apply deep learning to radiotherapy.

The validation and test sets were curated from CT planning scans selected from two open source datasets available from The Cancer Imaging Archive (Clark et al, 2013): TCGA-HNSC (Zuley et al, 2016) and Head-Neck Cetuximab (Bosch et al, 2015). Non-CT planning scans and those that did not meet the same slice thickness as the UCLH scans (2.5mm) were excluded. These were then manually segmented in-house according to the Brouwer Atlas (Brouwer et al, 2015). 31 scans were selected (22 Head-Neck Cetuximab, 9 TCGA-HNSC) which met these criteria, which were further split into validation (6 patients, 7 scans) and test (24 patients, 24 scans) sets. 

For more information on the original datasets please refer to the specific citations (Zuley et al, 2016; Bosch et al, 2015).

For more information on how this dataset and how it was created please refer to the artical that it accompanies (citation below).

## Selection of Organs At Risk
In order to select which OARs to include in the study, we used the Brouwer Atlas (consensus guidelines for delineating OARs for head and neck radiotherapy, defined by an international panel of radiation oncologists (Brouwer et al, 2015). From this, we excluded those regions which required additional magnetic resonance imaging for segmentation, were not relevant to routine head and neck radiotherapy, or that were not used clinically at UCLH. This resulted in a set of 21 organs at risk.

## Clinical Labelling and Annotation
To produce the ground truth labels the full volumes of all 21 OARs included in the study were segmented. This was done initially by a radiographer with at least four years experience in the segmentation of head and neck OARs and then arbitrated by a second radiographer with similar experience. Further arbitration was then performed by a radiation oncologist with at least five years post-certification experience in head and neck radiotherapy.

## Citation
To use this dataset please cite as follows:

@article{nikolov2018,
author = {Stanislav Nikolov and Sam Blackwell and Ruheena Mendes and Jeffrey De Fauw and Clemens Meyer and Cían Hughes and Harry Askham and Bernardino Romera-Paredes and Alan Karthikesalingam and Carlton Chu and Dawn Carnell and Cheng Boon and Derek D'Souza and Syed Ali Moinuddin and Kevin Sullivan and DeepMind Radiographer Consortium and Hugh Montgomery and Geraint Rees and Ricky Sharma and Mustafa Suleyman and Trevor Back and Joseph R. Ledsam and Olaf Ronneberger},
title = {Deep learning to achieve clinically applicable segmentation of head and neck anatomy for radiotherapy},
journal={arXiv preprint},
year = {2018},
}

## References
W. R.  Bosch,  W.  L.  Straube,  J.  W.  Matthews,  and  J.  A.  Purdy,  “Head-neck  cetuximab  -  thecancer  imaging  archive,”  2015.  Available:   https://wiki.cancerimagingarchive.net/display/Public/Head-Neck+Cetuximab

C. L. Brouwer,  R. J. H. M. Steenbakkers,  J. Bourhis,  W. Budach,  C. Grau,  V. Grégoire,  M. vanHerk,  A.  Lee,  P.  Maingon,  C.  Nutting,  B.  O’Sullivan,  S.  V.  Porceddu,  D.  I.  Rosenthal,  N.  M.Sijtsema,  and  J.  A.  Langendijk,  “CT-based  delineation  of  organs  at  risk  in  the  head  and  neckregion:   DAHANCA,  EORTC,  GORTEC,  HKNPCSG,  NCIC  CTG,  NCRI,  NRG  oncology  andTROG consensus guidelines,”Radiother. Oncol., vol. 117, no. 1, pp. 83–90, Oct. 2015. Available:http://dx.doi.org/10.1016/j.radonc.2015.07.041

K. Clark, B. Vendt, K. Smith, J. Freymann, J. Kirby, P. Koppel, S. Moore, S. Phillips, D. Maffitt,M.  Pringle,  L.  Tarbox,  and  F.  Prior,  “The  cancer  imaging  archive  (TCIA):  maintaining  andoperating a public information repository,”J Digit Imaging, vol. 26, no. 6, pp. 1045–1057, Dec.2013. Available: http://dx.doi.org/10.1007/s10278-013-9622-7

M. L. Zuley, R. Jarosz, S. Kirk, L. Y., R. Colen, K. Garcia, and N. D. Aredes, “Radiology data fromthe  cancer  genome  atlas  head-neck  squamous  cell  carcinoma  [TCGA-HNSC]  collection,”  2016. Available: http://dx.doi.org/10.7937/K9/TCIA.2016.LXKQ47MS

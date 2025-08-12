Forced-Aligned Diarization Labels for AMI and AliMeeting
===
This repository provides the diarization labels of the AMI and AliMeeting datasets obtained via forced alignment, used in our ASRU 2025 paper "Can We Really Repurpose Multi-Speaker ASR Corpus for Speaker Diarization?"
The labels are created using [Montreal Forced Aligner](https://montreal-forced-aligner.readthedocs.io/en/latest/#) with pretrained models.

Note that the provided labels are not perfect due to alignment errors, transcription ambiguity, out-of-vocabulary words, etc.
But at least, it is common to regard labels obtained via forced alignment as ground truth in VAD research (e.g., [[Kraljevski+, Interspeech 2025]](https://www.isca-archive.org/interspeech_2015/kraljevski15_interspeech.html) and [[Tan+, Computer Speech & Language 2020]](https://www.sciencedirect.com/science/article/abs/pii/S0885230819300920)).

## Annotations
### AMI
* The original dataset can be downloaded from [the official website](https://groups.inf.ed.ac.uk/ami/corpus/).
* The train/val/eval split follows the full-corpus ASR partition.
* We used the *only_words* setup, which only uses the intervals marked as words, not vocal sounds. Please refer to [BUTSpeechFIT/AMi-diarization-setup](https://github.com/BUTSpeechFIT/AMI-diarization-setup) for more details.
* For forced alignment, we first used [English (US) MFA G2P model v3.0.0](https://mfa-models.readthedocs.io/en/latest/g2p/English/English%20(US)%20MFA%20G2P%20model%20v3_0_0.html) to generate pronunciations for OOV words, and then used [English MFA acoustic model v3.1.0](https://mfa-models.readthedocs.io/en/latest/acoustic/English/English%20MFA%20acoustic%20model%20v3_1_0.html) and [English (US) MFA dictionary v3.1.0](https://mfa-models.readthedocs.io/en/latest/acoustic/English/English%20MFA%20acoustic%20model%20v3_1_0.html) for alignment.

### AliMeeting
* The original dataset can be downloaded from [OpenSLR](https://www.openslr.org/119/).
* For forced alignment, we first used [Mandarin (China) MFA G2P model v3.0.0](https://mfa-models.readthedocs.io/en/latest/g2p/Mandarin/Mandarin%20(China)%20MFA%20G2P%20model%20v3_0_0.html) to generate pronunciations for OOV words, and then used [Mandarin MFA acoustic model v3.0.0](https://mfa-models.readthedocs.io/en/latest/acoustic/Mandarin/Mandarin%20MFA%20acoustic%20model%20v3_0_0.html) and [Mandarin (China) MFA dictionary v3.0.0](https://mfa-models.readthedocs.io/en/latest/dictionary/Mandarin/Mandarin%20(China)%20MFA%20dictionary%20v3_0_0.html) for alignment.

## Citation
If you use our annotations, please cite [our paper](https://arxiv.org/abs/2507.09226) below.
```
@inproceedings{horiguchi_asru2025,
    author = {Horiguchi, Shota and Tawara, Naohiro and Ashihara, Takanori and Ando, Atsushi and Delcroix, Marc},
    title = {Can We Really Repurpose Multi-Speaker ASR Corpus for Speaker Diarization?},
    booktitle={IEEE Automatic Speech Recognition and Understanding Workshop (ASRU)},
    year = {2025},
    month = {Dec},
}
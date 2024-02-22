# Mark bad segments and channels

Brainlife App to reject bad data segments and/or channels MNE-Python [epo.info['bads']](https://mne.tools/stable/auto_tutorials/preprocessing/15_handling_bad_channels.html), and [mne.Annotations](https://mne.tools/stable/generated/mne.Annotations.html#mne-annotations).

# Documentation

#### Input files are:
* a MEG/EEG epochs file in fif format (mne/Epochs).

#### Input parameters are:
* ` Bads `:  str ,  The comma-separated channels to reject (e.g. "MEG2422,MEG2321").
* ` annotations `:  str , A multiline text describing segments to discard, following a format compatible with mne.Annotations:
    "start, duration, description[, channels]"

    For instance:
      
      2, 1, bad_segment
      5, 1, more_selective, MEG2422, MEG2321
      
    will create two annotations, one named "bad_segment" starting at 2s, with duration 1s, and second one named "more_selective" focused on channels MEG2422 and MEG2321, starting at 5s, with duration 1s.

#### Ouput files are:
  * the updated MEG/EEG file in fif format (mne/Epochs), where `epo.info['bads']` has been updated, and with added `epo.annotations`.

## Authors
- [Maximilien Chaumon](maximilien.chaumon@icm-institute.org)

## Contributors
- [Kamilya Salibayeva](ksalibay@iu.edu)


### Funding Acknowledgement
brainlife.io is publicly funded and for the sustainability of the project it is helpful to Acknowledge the use of the platform. We kindly ask that you acknowledge the funding below in your code and publications. Copy and past the following lines into your repository when using this code.

[![NSF-BCS-1734853](https://img.shields.io/badge/NSF_BCS-1734853-blue.svg)](https://nsf.gov/awardsearch/showAward?AWD_ID=1734853)
[![NSF-BCS-1636893](https://img.shields.io/badge/NSF_BCS-1636893-blue.svg)](https://nsf.gov/awardsearch/showAward?AWD_ID=1636893)
[![NSF-ACI-1916518](https://img.shields.io/badge/NSF_ACI-1916518-blue.svg)](https://nsf.gov/awardsearch/showAward?AWD_ID=1916518)
[![NSF-IIS-1912270](https://img.shields.io/badge/NSF_IIS-1912270-blue.svg)](https://nsf.gov/awardsearch/showAward?AWD_ID=1912270)
[![NIH-NIBIB-R01EB029272](https://img.shields.io/badge/NIH_NIBIB-R01EB029272-green.svg)](https://grantome.com/grant/NIH/R01-EB029272-01)

### Citations
1. Avesani, P., McPherson, B., Hayashi, S. et al. The open diffusion data derivatives, brain data upcycling via integrated publishing of derivatives and reproducible open cloud services. Sci Data 6, 69 (2019). [https://doi.org/10.1038/s41597-019-0073-y](https://doi.org/10.1038/s41597-019-0073-y)


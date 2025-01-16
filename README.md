# lipyd
A script that produces an untargeted lipid library from one or multiple DDA files

# Scope
This script will only use MS2 information from mgf files. It's recommended to use the library produced by this script in conjunction with MS1 peak picking software, and the output file is directly compatible with mzmine4.
The script is agnostic to the mass spectrometry platform as it purely uses the detected fragments. No parameter optimization is required.
This is just a script, not a package.

# Parameters

In rows 14-19, the user has to set a few parameters

MP_additive - mobile phase additive in the analysis. This can be either "Formate" or "Acetate". A string value.</br>
polarity - POS or NEG</br>
dir_base - the absolute path to the folder where the script and data files are wrapped in r'path' (e.g. r'/Volumes/name/lipyd/')</br>
mztol - this is to tolerance for mz in MS2 spectra, and dictates how much a detected fragment is allowed to deviate from the known exact value. I usually set this to 3.5 mmu (my instrument is QE HF-X at 60,000 resolution for MS2), but anything between 1.5-10 might be appropriate


# Usage
Download the script as well as LipidMatch rule-based lipid libraries. Create a virtual environment, and install dependencies via pip, conda, or alike.

# Settings for MSConvert
You can convert the raw mass spec data to .mgf's via MSConvert:
![image](https://github.com/user-attachments/assets/41167f3e-1844-4fc6-afae-ad7680747e7d)

# Dependencies
LipidMatch lipid libraries.<br/> 
Python 3.10.9 <br/>
pandas 1.5.3 <br/>
polars 1.5.0 <br/>
pyteomics 4.6 <br/>


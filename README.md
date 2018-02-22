# ICD10Codes
A tab-delimited file that contains the full names of each ICD-10 Code

You might use it like this in python to create a dictionary mapping ICD-10 codes to name:


```
import pandas as pd
with open('icd10codes_2016_parsed.tsv' , 'rb') as file:
    icd10names = pd.read_csv(file,sep='\t',header = None)    
icd10names = dict(zip(icd10names[0],icd10names[1]))
```

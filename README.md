# Python 

## Importing Excel 
```import pandas as pd
xl = pd.ExcelFile("Entity.xlsx")
```
### Checking the sheets in the  excel
```
xl.sheet_names
```
### Saving the sheet in to the Data Frame
```
df = xl.parse("Sheet1")
```
### Removing the NA values
```
r=df["Region"]
r.dropna(inplace=True)
```
## Dictionarie

## Setting key value for the data set
```
rv="region"
d1={l:rv for l in r }
```

## Merging 2  Dictionaries
```
d1.update(d2)
```

## removing the extra spaces in the sentence
```
sentence = ' hello     apple hjdfs    ads'
a=" ".join(sentence.split())
```

## Pickiling the  Dictionaries
```
import pickle
f = open("enlist.pkl","wb")
pickle.dump(d2,f)
f.close()
```
## Un-Pickiling the  Dictionaries

```
e=pickle.load(open("enlist.pkl","rb"))
print(e['Display'])
```

## removing spaces before wwords
```
proper_entity=[[l[0].strip()]for l in proper_entity]
```
## Adding spaces
```
def clean_sentence(sent):
    text = str(sent)
    text = text.replace('/', " / ")
    text = text.replace('-', ' - ')
    text = text.replace('&', ' & ')
    text = text.replace('?', " ?")
    text = text.replace(',', " , ")
    text = text.replace('\t', " ")
    text = text.replace('\n', " ")
    text = text.replace('$', " $ ")
    return text
```

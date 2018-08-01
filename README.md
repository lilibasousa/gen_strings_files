gen_strings_files
--------------------

This script generates strings files for different languages based on a CSV file.

# Set up

## CSV file with the translations
You will need a csv file with the translations.  
You can export to csv from an excel, for instance.  

```bash
string1_key,string1_in_language1,...,string1_in_languageN
string2_key,string2_in_language1,...,string2_in_languageN
...
stringM_key,stringM_in_language1,...,stringM_in_languageN
```
 
### Example:
See examples/source.csv

```bash
string_hello,hello,ola,ciao
string_good_morning,good morning,bom dia,buongiorno
string_bye,bye,adeus,arrivederci
string_dinner,dinner,jantar,cena
```


## Config file with the languages to generate
You will need a csv file with the config for the files you want to generate.   
There you will need to specify, per line, the language you want to generate and in  which column of the source.csv you have the value for it.    

```bash
language1,column_for_language1
...
languageN,column_for_languageN
```

### Example:
See examples/config.csv

```bash
en,2
pt,3
it,4
```

# Running the scripts
To generate the strings files use:
```bash
gen_strings_files programming_language config_file source_file
```

### Examples:
```bash
gen_strings_files iOS examples/config.csv examples/source.csv
gen_strings_files Android examples/config.csv examples/source.csv
```

At the moment only iOS and Android are supported.   
The result files will be under the folder named "results".   
To remove this folder, you can use the script with clear as param:   
```bash
gen_strings_files clear
```


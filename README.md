gen_strings_files
--------------------

This script generates strings files for different languages based on a CSV file.

# Set up

## CSV file with the translations
```bash
<string1_key>,<string1_in_language1>,...,<string1_in_languageN>
<string2_key>,<string2_in_language1>,...,<string2_in_languageN>
...
<stringM_key>,<stringM_in_language1>,...,<stringM_in_languageN>
```
 
### Example:
```bash
string_hello,hello,ola,ciao
string_good_morning,good morning,bom dia,buongiorno
```


## Config file with the languages to generate
```bash
<language1>,<column for language1>
...
<languageN>,<column for languageN>
```

### Example:
```bash
en,2
pt,3
it,4
```

# Running the scripts
```bash
gen_strings_files <programming_language> <languages>
```

### Examples:
```bash
gen_strings_files iOS pt,it
gen_strings_files Android it
```

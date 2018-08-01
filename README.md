gen_strings_files
--------------------

This script generates strings files for different languages based on a CSV file.

# Set up

## CSV file with the translations
```bash
<string1 key>,<string1 in language1>,...,<string1 in languageN>
<string2 key>,<string2 in language1>,...,<string2 in languageN>
...
<stringM key>,<stringM in language1>,...,<stringM in languageN>
```
 
### Example:
string_hello,hello,ola,ciao
string_good_morning,good morning,bom dia,buongiorno


## Config file with the languages to generate
```bash
<language1>,<column for language1>
...
<languageN>,<column for languageN>
```

### Example:
en,2
pt,3
it,4

# Running the scripts
gen_strings_files <programming_language> <languages>

### Examples:
gen_strings_files iOS pt,it
gen_strings_files Android it

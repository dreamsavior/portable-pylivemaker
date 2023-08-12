# portable-pylivemaker
Portable pylivemaker for windows system

Visit pylivemaker: https://pylivemaker.readthedocs.io/en/latest/readme.html

## Usage
See the complete documentation on how to use pylivemaker here : https://pylivemaker.readthedocs.io/en/latest/usage.html

### 1. Extract the game
```shell
.\Python\Scripts\lmar.exe x 'path\to\the\game.exe' -o 'path\to\the\extracted\directory'
```

### 2. Dump the translatable texts inside lsb into csv
```shell
.\Python\Scripts\lmlsb.exe --encoding=utf-8-sig 'path\to\the\extracted\directory\00000001.lsb' 'path\to\the\translatable\00000001.csv'
```

### 3. Edit the CSV using your prefered spreaadsheet.
The translation is at the column E

### 4. Patch back the LSB with the translated CSV
```shell
.\Python\Scripts\lmlsb.exe insertcsv --encoding=utf-8-sig 'path\to\the\extracted\directory\00000001.lsb' 'path\to\the\translatable\00000001.csv' 
```

### 5. Patch the exe with the translated LSB
```shell
.\Python\Scripts\lmpatch.exe 'path\to\the\game.exe' 'path\to\the\extracted\directory\00000001.lsb' 
```


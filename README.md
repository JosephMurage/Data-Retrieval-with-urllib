---

# Web Data Retrieval with urllib

This repository contains Python scripts demonstrating web data retrieval using the `urllib` library. The scripts provided here allow users to read data from web links and perform various operations on the retrieved data.

## Scripts

### 1. retrieve_html_file.py

This script retrieves and prints the HTML content of a web page located at http://www.dr-chuck.com/pae1.htm.

```python
import urllib.request, urllib.parse, urllib.error

file_handle = urllib.request.urlopen ('http://www.dr-chuck.com/pae1.htm')
for line in file_handle:
    print (line.decode().strip())
```

### 2. retrieve_line_in_txt.py

This script retrieves and prints the lines of text from a web page located at http://data.pr4e.org/romeo.txt.

```python
import urllib.request, urllib.parse, urllib.error

file_handle = urllib.request.urlopen('http://data.pr4e.org/romeo.txt')

for line in file_handle:
    print(line.decode().strip())
```

### 3. word_count_in_line.py

This script retrieves the lines of text from a web page located at http://data.pr4e.org/romeo.txt and counts the occurrences of each word.

```python
import urllib.request, urllib.parse, urllib.error

file_handle = urllib.request.urlopen('http://data.pr4e.org/romeo.txt')
counts = dict()
for line in file_handle:
    words = line.decode().split()
    for word in words:
        counts[word] = counts.get(word, 0) + 1
print(counts)
```

## Usage

To use these scripts, make sure you have Python installed on your system. You can run each script individually by executing the corresponding Python file using a Python interpreter.

```bash
python retrieve_html_file.py
python retrieve_line_in_txt.py
python word_count_in_line.py
```

---
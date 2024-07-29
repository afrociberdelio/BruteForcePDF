## Cracking password PDF files

### Clone Lab
```git clone https://github.com/afrociberdelio/BruteForcePDF.git```

### Install requirements to Lab
- [Python 3.12](https://www.python.org/downloads/release/python-3120/) ou superior  
```pip install requirements.txt```

### Get hash to PDF file (Powershell)
```cd hashcat```  
```python pdf2john.py "path/yourfile.pdf" | Out-File -FilePath pdf_hash.txt -Encoding UTF8```

### Crack password with 4 numeric digits
```hashcat.exe -a 3 -m 10600 .\pdf_hash.txt ?d?d?d?d```

<img src="https://miro.medium.com/v2/resize:fit:2000/format:webp/0*sw_2l_KnwEQmKVUg" alt="sample cracked password">

https://hashcat.net/wiki/doku.php?id=mask_attack

https://hashcat.net/wiki/doku.php?id=example_hashes

https://github.com/hashcat/hashcat/releases/tag/v6.2.6

https://github.com/unstable-deadlock/brashendeavours.gitbook.io/blob/master/pentesting-cheatsheets/hashcat-hash-modes.md
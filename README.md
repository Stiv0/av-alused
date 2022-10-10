# NETWORKING FOR WEB DEVELOPERS

## LESSON 1

Kohe esimese pingimise ülesande jaoks oli vaja Linuxi masinasse installida selleks vajalik tööriist käsuga ``sudo apt install iputils-ping``

Pingimisega saab teada, kas selle IP-ga on ühendus olemas.

Käsuga ``printf 'HEAD / HTTP/1.1\r\nHost: en.wikipedia.org\r\n\r\n' | nc en.wikipedia.org 80`` saadetakse netcatiga Wikipedia serverile printf funktsiooni poolt väljastatud string, mis on HTTP request, ja veebiserver saadab vastu HTTP response headeri, mis sisaldab infot, mida HTTP requestiga küsiti.




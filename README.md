# NETWORKING FOR WEB DEVELOPERS

## LESSON 1

Kohe esimese pingimise ülesande jaoks oli vaja Linuxi masinasse installida selleks vajalik tööriist käsuga ``sudo apt install iputils-ping``

Pingimisega saab teada, kas selle IP-ga on ühendus olemas.

Käsuga ``printf 'HEAD / HTTP/1.1\r\nHost: en.wikipedia.org\r\n\r\n' | nc en.wikipedia.org 80`` saadetakse netcatiga Wikipedia serverile printf funktsiooni poolt väljastatud string, mis on HTTP request, ja veebiserver saadab vastu HTTP response headeri, mis sisaldab infot, mida HTTP requestiga küsiti.

Kui me tunnis rääkisime, et IP-aadress on võrreldav pärismaailmas koduaadressiga, siis pordinumber on justkui korterinumber, mis täpsustab, millise ukse taga server parajasti on valmis ühendust vastu võtma (*listening*). Pordinumbrite vahemik on 0 kuni 65535.
Käsklusega ``sudo lsof -i`` saab vaadata, mis programmid hetkel kuulavad.

Lihtsa serveri näitena saab netcatiga panna masina kuulama mingi pordi peale käsuga ``nc -l 1234`` ja siis teises terminalis ühendada selle külge käsuga ``nc localhost 1234``. Localhost viitab kohaliku arvuti IP-aadressile ning pordinumber näitab, millise liini külge ühendada. See loob kahe terminali vahel TCP ühenduse, mis on justkui telefonikõne, mõlemad pooled saavad üksteisega suhelda samaaegselt ning mõlemad pooled saavad ühenduse ka katkestada. Terminalis saab selle ühenduse katkestada vajutades Ctrl + D.

## LESSON 2

DNS record types
- CNAME record ehk canonical name on lihtsam variant nimest, mis viitab tegelikule domemeeninimele
- AAAA ja A record näitavad domeeninimele kuuluvat IP-aadressi, AAAA näitab IPv6 ja A näitab IPv4
- NS record näitab, mis nimeserverist vastava domeeni IP-aadressi leiab


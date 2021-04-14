### 1. Tehtävä
Haku ei löydä "sisu" nimellä mitään mutta lähin mahdollinen on "sisulia"

| Syntynyt     | Kastettu         | Kylä   | Talo   | Isä  | Äiti |Lapsi  |
| -------------|:----------------:| ------:|-------:|-----:|-----:|------:|
| 10.11.1887   | 13.11.1887       | Kojo   |	Iso-Pietilä p.258 | Iso-Pietilän omistaja Kalle Oskar Erkinp. Anttila | Hilma Karolina Kustaantr  | 	Hilja Sisulia |

### 2. Tehtävä
Olen tehnyt käyttäjiä useisiin palveluihin joita en enään käytä. yleensä palveluihin kirjautuessa ei tarvita henkilökohtaisia tietoja kuten syntymäpäivää tai nimeä mutta johonkin henkilökohtaisempiin palveluihin tarvitaan. Oman nimeni olen laittanut palveluihin mutta syntymäpäivän olen lähes aina vaihtanut syystä tai toisesta.

### 3. Tehtävä

### 4. Tehtävä
Vataus: SELECT * FROM Kurssisuoritus

### 5. Tehtävä
Vataus: SELECT kurssi * FROM Kurssisuoritus

### 6. Tehtävä
Vataus: SELECT DISTINCT kurssi FROM Kurssisuoritus

### 7. Tehtävä
Vataus: SELECT * FROM Opiskelija WHERE nimi = 'Anna'

### 8. Tehtävä
Vataus: SELECT * FROM Kurssisuoritus WHERE opiskelija = 'Pihla'

### 9. Tehtävä
Vataus: SELECT * FROM Opiskelija WHERE pääaine  LIKE '%tiede%'

### 10. Tehtävä
Vataus: SELECT Kurssi.nimi, Kurssisuoritus.päivämäärä, kurssisuoritus.arvosana
        FROM Kurssi, Kurssisuoritus
        WHERE Kurssi.kurssitunnus = Kurssisuoritus.kurssi
        
### 11. Tehtävä
Vataus: SELECT Opiskelija.nimi, Kurssisuoritus.päivämäärä, kurssisuoritus.arvosana 
        FROM Opiskelija, Kurssisuoritus 
        WHERE Opiskelija = Kurssisuoritus.Opiskelija


        


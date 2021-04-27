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

### 12. Tehtävä
Vataus: SELECT Kurssi.nimi AS kurssi, Kurssitehtävä.tehtävä AS tehtävä
        FROM Kurssitehtävä, Kurssisuoritus, Kurssi
        
### 13. Tehtävä
Vataus: SELECT Opiskelija.nimi AS Opiskelija, Kurssi.nimi AS Kurssi, Tehtävä.nimi AS Tehtävä
    FROM Kurssi, Kurssitehtävä, Tehtävä, Tehtäväsuoritus, Opiskelija
    WHERE Kurssi.nimi = 'Tietokantojen perusteet'
        AND Kurssi.kurssitunnus = Kurssitehtävä.kurssi
        AND Tehtävä.tunnus = Kurssitehtävä.tehtävä
        AND Tehtäväsuoritus.tehtävä = Kurssitehtävä.tunnus
        AND Tehtäväsuoritus.opiskelija = Opiskelija.opiskelijanumero
        AND Opiskelija.nimi = 'Anna'
        
### 14. Tehtävä
Koska useampi ihminen on tehnyt saman tehtävän.

### 15. Tehtävä
Vataus: SELECT kurssi FROM kurssisuoritus o
        WHERE o.kurssi
        NOT IN (SELECT opiskelija FROM Kurssisuoritus)
 
### 16. Tehtävä
Vataus: SELECT kurssi AS kurssikoodi, COUNT(*) AS lukumäärä
        FROM Kurssisuoritus GROUP BY kurssi

### 17. Tehtävä
Vataus: SELECT Kurssi.nimi AS kurssi, COUNT(*) AS lukumäärä
        FROM Kurssisuoritus, Kurssi 
        WHERE Kurssi.kurssitunnus = Kurssisuoritus.Kurssi
        GROUP BY kurssi
        
### 18. Tehtävä
Vataus: SELECT k.nimi AS kurssi, COUNT(ks.kurssi) as lukumäärä FROM Kurssi k LEFT JOIN Kurssisuoritus ks
        ON k.kurssitunnus = ks.kurssi GROUP BY k.nimi

### 19. Tehtävä
Vataus: CREATE TABLE Kurssi (kurssitunnus, nimi, kuvaus)
        
### 20. Tehtävä
Vataus: INSERT INTO Kurssi (kurssitunnus, nimi, kuvaus)
        VALUES (12345, 'SQL-kielen perusteet', 'Select "Hei maailma"')

### 21. Tehtävä
Vataus: CREATE TABLE Testi (Moi, Hei, Terve)

### 22. Tehtävä
Vataus: CREATE TABLE Kurssi (kurssitunnus integer, nimi varchar(200), kuvaus varchar(200))

### 23. Tehtävä
Vataus: Saman nimisiä opiskelijoita lisääntyy useita mutta opiskelija numero kasvaa aina yhdellä

### 24. Tehtävä
Vataus: CREATE TABLE Kurssi (kurssitunnus integer PRIMARY KEY, nimi varchar(100), kuvaus varchar(100))

### 25. Tehtävä
Vataus: CREATE TABLE Tehtävä
        (
        tunnus integer PRIMARY KEY,
        nimi varchar(200) NOT NULL
        );
        CREATE TABLE Kurissitehtävä
        (
        tehtävä integer, 
        kurssi integer,
        FOREIGN KEY(tehtävä) REFERENCES Tehtävä(tunnus)
        FOREIGN KEY(kurssi) REFERENCES Kurssi(kurssitunnus)
        )
        
### 26. Tehtävä
Vataus: INSERT INTO Tehtävä(nimi) VALUES("Tietoturva");
        INSERT INTO Tehtävä(nimi) VALUES("Tietotekniikka");
        
### 27. Tehtävä
Vataus: ALTER TABLE:n avulla voidaan lisätä, poistaa ja muokata olemassa olevia tauluja. Sillä voidaan myös luoda niihin rajoituksia.

ADD komennolla voidaan lisätä pylväitä
````
ALTER TABLE Customers
ADD Email varchar(255);
````


        


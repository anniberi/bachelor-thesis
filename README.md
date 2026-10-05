# Distributed State Estimation Using Gaussian Belief Propagation

Bachelor's thesis exploring how the Gaussian Belief Propagation (GaBP) algorithm lets nodes in a distributed network estimate system state by passing local messages, without a central processor. The thesis derives the mathematics behind GaBP and shows that it is equivalent to solving a system of linear equations. It then walks through a complete numerical example and ends with a MATLAB implementation.

> **Note:** Apart from this summary, everything in this project is written in Bosnian: the rest of this README, the source code, the comments and the technical documentation.

> **Napomena:** Izvorni kod, komentari i tehnička dokumentacija za ovaj projekat su napisani na bosanskom jeziku.

## O projektu

Ovaj repozitorij sadrži završni rad prvog ciklusa studija pod naslovom **„Distribuirana estimacija stanja korištenjem Belief Propagation algoritma"**. Rad je odbranjen na Odsjeku za automatiku i elektroniku Elektrotehničkog fakulteta Univerziteta u Sarajevu u septembru 2022. godine.

Procjena stanja sistema na osnovu mjerenja s velikog broja čvorova može se provoditi centralizirano ili distribuirano. Centralizirani pristupi su pogodni za manje mreže, dok se distribuirani algoritmi pokazuju efikasnijim kada mreža ima veliki broj čvorova. Rad predstavlja osnove Gaussian Belief Propagation (GaBP) algoritma kao primjera distribuiranog pristupa. Pitanje konvergencije algoritma, koje je znatno složenije, ostavljeno je izvan opsega rada.

## Sadržaj rada

1. **Uvod**: motivacija za problem procjene stanja i razlika između centraliziranih i distribuiranih algoritama.
2. **Opis problema**: definicija Belief Propagation algoritma, linearni Gausov model opservacija na svakom čvoru, Gausovo Markovljevo slučajno polje (MRF), faktor grafovi i razmjena poruka između čvorova.
3. **Opis algoritma**: pokazuje se da je GaBP ekvivalentan rješavanju sistema linearnih jednačina **Ax = b** za simetričnu pozitivno definitnu matricu **A**, te se opisuje postupak koji se može direktno implementirati u programskom jeziku.
4. **Numerički primjer**: rješava se sistem od pet jednačina s pet nepoznatih. Prikazane su vrijednosti svih značajnih varijabli u svakoj iteraciji do konvergencije, te se pokazuje da dobiveni vektor predstavlja egzaktno rješenje.
5. **Zaključak**: sažetak rezultata i prijedlozi za proširenje rada.
6. **Prilog A**: implementacija algoritma u MATLAB-u.

## Metodologija

- Polazi se od linearnog Gausovog modela opservacija na svakom čvoru mreže i od procjene minimalne srednjekvadratne greške u centraliziranom slučaju.
- Zajednička funkcija vjerovatnoće izražava se preko faktor grafa, nad kojim čvorovi iterativno razmjenjuju poruke i ažuriraju svoja vjerovanja (engl. *beliefs*).
- Problem statističke inferencije svodi se na minimizaciju kvadratne funkcije, odnosno na rješavanje sistema linearnih jednačina.
- Ispravnost postupka provjerava se na numeričkom primjeru, čije se rješenje poredi s egzaktnim rješenjem sistema.

## Struktura repozitorija

| Datoteka | Opis |
|---|---|
| `Zavrsni_rad___finalna_verzija.pdf` | Finalna verzija završnog rada (30 stranica) |

## Korištenje

Rad je dostupan u PDF formatu i može se otvoriti u bilo kojem PDF čitaču. MATLAB kod iz Priloga A može se prepisati u MATLAB ili GNU Octave i pokrenuti bez dodatnih paketa. Kod rješava sistem iz numeričkog primjera iz četvrtog poglavlja.

## Autor

- **Autor:** Berina Biberović
- **Mentor:** Dr Mirsad Ćosović, docent
- **Ustanova:** Elektrotehnički fakultet, Univerzitet u Sarajevu, Odsjek za automatiku i elektroniku
- **Godina:** 2022.

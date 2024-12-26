# olympic_db

Hei ope tein tietokannan kuvitteellisista olympialaisista, jossa on seuraavat taulukot:

SPORTS:
sport_id INT - lajin sarjanumero

urheilun_nimi VARCHAR(255) - lajin nimi (koripallo jne.)

luokka VARCHAR(255) - urheiluluokka (joukkue, yksittäinen)

sukupuoli VARCHAR(255) - sukupuoli (mies, nainen)

kausi VARCHAR(255) - kausi (talvi, kesä)

COUNTRY:

country_id SERIAL - maan sarjanumero

maan_nimi VARCHAR(255) - maan nimi (Suomi, Ukraina jne.)

ATHLETES:

athletes_id SERIAL - urheilijan sarjanumero

etunimi VARCHAR(255) - nimi

sukunimi VARCHAR(255) - sukunimi

country_id INT - urheilijan maan sarjanumero (liittyy MAAT-taulukkoon)

sport_id INT - urheilijan sarjanumero (liittyy ATHLETES-taulukkoon)

games_id INT - sen pelin sarjanumero, johon urheilija osallistuu (liittyy GAMES-taulukkoon)

sukupuoli VARCHAR(255) - sukupuoli

paino SMALLINT - paino (kg)

korkeus SMALLINT - korkeus (senttiä)

GAMES:

games_id SERIAL - kilpailun sarjanumero

games_date DATE – kilpailun päivämäärä

country_id INT - sen maan sarjanumero, jossa kilpailu pidettiin (liittyy MAA-taulukkoon)

urheilijat_id INT[] - tämän vuoden kilpailuihin osallistuneiden Yaui-urheilijoiden järjestysmäärä (liittyy ATHLETES-taulukkoon)

tiedoston lopussa on 4 esimerkkiä vuorovaikutuksesta tietokannan kanssa

p.s. Pahoittelen, että tiedosto on .txt-tunnisteella, git ei jostain syystä nähnyt sql-tiedostoa, toivottavasti sinulla oli ihana joulu ja onnellista uutta vuotta

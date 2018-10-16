# BA-Logisztika - Java állás interjú feladat

## Leírás
Készíts egy alkalmazást, mely HTTP protokoll segítségével képes cikkek mentésére, megjelenítésére és listázására.  
A megvalósítás adatbázistól egészen REST API-ig terjedjen, és legyenek unit tesztek is, valmaint tartalmazzon exception kezelést. Felhasználói felület készítése nem része a feladatnak!

## Szerkezet

### Cikk (Article) szerkezete (adatbázis):
* **id** INTEGER (UNIQUE, PRIMARY_KEY, NOT_NULL)
* **title** VARCHAR(255) (NOT_NULL)
* **text** TEXT (NOT_NULL)

### REST API Végpontok:
* **/api/article/list:** **GET** metódus segítségével listázza ki **JSON** formátumban az összes cikk azonosítóját (*id*) és címét (*title*)
* **/api/article/save:** **POST** metódus segítségével bekér egy cikket (*title* és *text*, **JSON** formátumban), majd elmenti azt az adatbázisban.
* **/api/article/{id}:** **GET** metódus segítségével jelenítse meg az url-ben szereplő azonosítóval (*id*) rendelkező cikk címét (*title*) és szövegét (*text*), valamint a cikkben szereplő szavak számát (ezt ne tárolja adatbázisban, hanem számított érték legyen!)

## Használandó technológiák
* Spring Boot 2+
* Spring Data JPA vagy MyBatis
* Spring REST
* PostgreSQL 9.6
* JDK 8
* JUnit 4
* Maven vagy Gradle

## Beadás menete
Az elvégzett feladatot ebbe a repositoryba töltsd fel. Akár több commit is elfogadott, az értékelésnél a master branch utolsó commitját fogjuk értékelni.
A feladat befejezése után küldj értesítést az alábbi címre: <fejlesztes@ba-logisztika.hu>

## Információ
* A végpontok Postman-nel lesznek tesztelve.

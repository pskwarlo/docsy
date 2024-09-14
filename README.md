 ### Symulator systemu kontroli dostępu RFID 
 Symulator systemu kontroli dostępu RFID umożliwia:
 * dodawanie czytnika do bazy 
 * przypisanie czytnika do drzwi 
 * dodanie listy użytkowników upoważnionych do wejścia do pomieszczenia  
 * przypisanie ID taga do danego użytkownika 
 * tworzenie harmonogramów dostępu
 

Projekt korzysta z bazy danych PostgreSQL: 
https://www.postgresql.org/download/
Dokumentacja znajduję się na GitLab Wiki:
https://git.pg.edu.pl/pos_ikb/rfid_system/-/wikis/home

Aby poprawnie uruchomić  projekt należy:
* otworzyć projekt w Eclipse lub Visual Code
* skonfigurować bazę danych PostgreSQL
* W pliku AccesssController.java uzupełenić informacje dotyczące bazy danych tj. DB_URL
USER
PASS
* Wejść do ustawień run configuration i podać parametry startowe dla aplikacji RFIDReadrerSimulator np.: --reader.name = "reader1"  --server.port=8081 
* Powtórzyć poprzedni krok dla kolejnych instancji czytników
* Uruchomić aplikację RFIDReaderSimulator
* Uruchomić aplikację RFIDServer
* Uruchomić aplikację RFIDServerWebInterface (domyślnie uruchamia się na localhost:8080)
* W przeglądarce połączyć się z localhost:8080 i za pomocą GUI korzystać z funkcjonalności systemu.
* Poprawność działania można sprawdzić łącząc się na localhost:8081 i weryfikując czy do czytnika reader1 mają dostęp tylko uprawnione tagi 

# Symulator systemu kontroli dostępu RFID
To repozytorium zawiera `Symulator systemu kontroli dostępu RFID` oraz aplikację serwerową wymaganą do poprawnego działania oprogramowania.

## Uruchomienie aplikacji 
- [Ściągnij repozytorium](https://docs.github.com/en/repositories/working-with-files/using-files/downloading-source-code-archives) 
- Pobierz i zainstaluj [PostgreSQL](https://www.postgresql.org/download/)
- Otwórz projekt w środowisku [Visual Code](https://learn.microsoft.com/en-us/visualstudio/install/install-visual-studio?view=vs-2022) lub [Eclipse](https://www.eclipse.org/downloads/packages/installer) 
- Otwórz plik [`AccessController.java`](https://git.pg.edu.pl/pos_ikb/rfid_system/-/blob/master/src/main/java/com/example/demo/AccessController.java)
- W `AccessController.java` uzupełnij pola:
	- `USER`
	- `PASS`
	- `DB_URL`
- W środowisku przejdź do `RUN -> Configuration` i uzupełnij parametry startowe dla aplikacji `RFIDReadrerSimulator`
- Jeżeli chcesz skonfigurować więcej niż jeden czytnik powtórz poprzednik krok z innymi parametrami
- Uruchom aplikację `RFIDReaderSimulator`, `RFIDServer` oraz `RFIDServerWebInterface` - domyślnie uruchamiana na `localhost:8080`
- W przeglądarce internetowej uruchom `localhost:8080`, od teraz dostęp do aplikacji odbywa się za pomocą GUI
- Poprawność działania można sprawdzić łącząc się na localhost:8081 i weryfikując czy do czytnika reader1 mają dostęp tylko uprawnione tagi
## Dokumentacja 
Dokumentacja kodu źródłowego znajduje się w folderze [Docs](https://www.doxygen.nl/download.html), zawiera ona opis zadania każdej klasy, metody i funkcji publicznych oraz ogólny zarys struktury projektu. 

Aby wygenerować dokumentację z kodu źródłowego należy:
## Generowanie dokumentacji 
Aby wygenerować dokumentację z kodu źródłowego należy:
## Zakładka Wizard
### W topicu `Project`
- Zainstalować [Doxygen](https://git.pg.edu.pl/pos_ikb/rfid_system/-/tree/master/bin), uruchomić program 
- W pierwszym polu wskazać ścieżkę w której będzie uruchomiony Doxygen 
- W polu `Project name` wpisać nazwę projektu 
- W polu `Source code directory` wskazać ścieżkę do kodu źródłowego  
- Zaznaczyć `Scan recursively` 
- W polu `Destination directory` wprowadzić miejsce w którym ma zostać wygenerowana dokumentacja 
### W topicu `Mode`
- Zaznaczyć `Optimize for Java or C# output`
### W topicu Output
- Wybrać format w jakim ma być wygenerowana dokumentacja (`HTML` lub `LaTeX`)

## Zakładka Run
- Kliknąć `Run doxygen`, poczekać na wygenerowanie dokumentacji 
- Wygenerowana dokumentacja znajduje się w folderu wskazany w polu `Destination directory`

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

# Projekt Szachowy (Klient i Serwer)
 
## Opis Projektu
Projekt Szachowy to aplikacja umożliwiająca rozgrywkę w szachy z wykorzystaniem architektury klient-serwer. Na serwerze znajdują się pliki niezbędne do uruchomienia gry (np. na AWS), natomiast klient zawiera interfejs umożliwiający grę na stacji roboczej. Projekt został napisany w Pythonie 3, z użyciem bibliotek "pygame" oraz "chess", a także korzysta z silnika Stockfish w osobnym pliku.
 
## Zawartość Repozytorium
- Folder z plikami serwera (deployowany na AWS lub innym serwerze)
- Folder `client` zawierający pliki niezbędne do działania interfejsu klienta
 
## Instrukcja Instalacji i Uruchomienia
 
### Dla dystrybucji opartych na Debianie (Linux)
 
1. Zainstaluj Python 3:
   sudo apt install python3
 
2. Zainstaluj wymagane biblioteki:
   pip install chess  
   pip install pygame
 
3. Uruchom aplikację wykonując:
   python3 chesspy.py
 
### Dla Windows
 
1. Zainstaluj Python 3 pobierając go z: https://www.python.org/downloads
 
2. Zainstaluj wymagane biblioteki:
   pip install pygame
 
3. Uruchom aplikację wykonując:
   python chesspy_windows.py
 
   Uwaga: Różnica pomiędzy plikami "chesspy.py" oraz "chesspy_windows.py" polega na użyciu osobnego pliku zawierającego silnik Stockfish.
 
### Instrukcja Konfiguracji Klienta
 
1. Pobierz pliki z folderu `client` na swoją stację roboczą.
 
2. Zainstaluj Python 3:  
   Dla Windows można pobrać ze strony: https://www.python.org/downloads/
 
3. Uruchom terminal w folderze `client` i zainstaluj wymagane biblioteki:
   pip install pyinstaller  
   pip install pygame  
   pip install chess
 
4. Stwórz plik wykonywalny przy użyciu polecenia:
   python -m PyInstaller client.spec  
   Polecenie to zainstaluje wersję .exe w folderze `dist`.
 
5. W folderze obok wygenerowanego pliku .exe skopiuj folder `pieces` zawierający grafiki przedstawiające figury szachowe.
 
## Serwer
 
Pliki serwera są udostępniane na serwerze gry (np. AWS). Obecnie serwer dostępny jest pod adresem IP: 13.38.13.177. Aby korzystać z serwera, skopiuj pliki z folderu klienta na swoją stację roboczą, a następnie wykonaj powyższe kroki konfiguracji klienta.
# Eksport pliku tłumaczenia z plików gry.

1. Pobieramy narzędzie Fmodel i wybieramy w nim ścieżkę do plików gry (do folderu z głównym plikiem .exe)

![image](https://github.com/Shieldowskyy/spolszczenie-fnaf-sb/assets/32707076/27642dfb-7230-47c4-8d94-31c1f46945d1)

2. Dodajemy klucz AES który odszyfruje pakiet z plikami gry. Klucz: ```0x85F7D4007015493ED0359C9007266038F8F7B1F96988F19A610103874CC95286```

![image](https://github.com/Shieldowskyy/spolszczenie-fnaf-sb/assets/32707076/d308401a-b7f7-4ee7-b533-f5421b0e58e1)

3. Otwieramy plik pak 'fnaf9-WindowsNoEditor.pak' i w katalogu Localization/DLC/en znajdziemy plik ze wszystkimi wpisami

![image](https://github.com/Shieldowskyy/spolszczenie-fnaf-sb/assets/32707076/099c1c20-9116-4ec2-80b4-a871f697c92d)

4. Klikamy na niego prawym i wybieramy opcję Export Raw Data

![image](https://github.com/Shieldowskyy/spolszczenie-fnaf-sb/assets/32707076/f76b6c7b-6e8e-44b7-b1df-3d1ec890bbb3)


# Eksport plików do formatu .po
Aby wyeksportować plik do formatu obsługiwanego przez program PoEdit, należy użyć dołączonego narzedzia UnrealLocres. Uruchamiany powershell i robimy tak:

1. Przechodzimy do lokalizacji z plikami .locres oraz programem UnrealLocres używając komendy np. ```cd C:\lokalizacja\plikow\```

2. Następnie narzędziem UnrealLocres konwertujemy plik z formatu .locres do formatu .po co zrobimy używając komendy ```./UnrealLocres.exe export DLC.locres -f pot```

3. W katalogu powinien się teraz znajdować plik DLC.po który będzie można normalnie edytować używając programu Poedit!

# Edycja plików
Aby edytować zawarte pliki źródłowe należy użyć **programu do edycji plików .po**
Przykładowym programem który ja użyłem był program **Poedit** dostępny za darmo na tej stronie: https://poedit.net/
<br />W prosty sposób otworzy on nam plik i pozwoli na jego łatwą edycję oraz zapobiegnie popełnieniu typowych błędów składniowych.
**Nie ma potrzeby kupowania wersji Pro** ponieważ do tłumaczenia maszynowego wystarczy przeklejać ręcznie frazy do Tłumacza Google/Deepl.

# Najlepsze praktyki
W jednym z patchy, SteelWood zmieniło sposób wyświetlania dialogów w grze przez co należy edytować tylko rekordy z Timmingami tj. "\_00_00 " itp.
<br />Edytowanie innych typów nie będzie działało poprawnie i nie zobaczysz efektów po wejściu do gry.
Sprawia to również że **nie** należy się sugerować wartością procent przetłumaczonych rekordów ponieważ część i tak pomijamy.
Polecam również pomijać rekordy które są wycięte w finalnej grze np. dialogi z trybu Survival, ponieważ to strata czasu.

Ważne jest aby nie zmieniać/usuwać nagłówków tekstowych np. w dialogach! (np. wartość "\_00_00 " musi pozostać taka sama!).

# Obsługa Polskich Znaków
Polskie znaki najwyraźniej są obsługiwane przez większość czcionek w grze więc nie trzeba się ich pozbywać ani modyfikować słów.

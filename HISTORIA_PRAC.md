# Historia prac nad Vilianem

Stan na 20 listopada 2026 r.

## Październik — prototyp i pierwsze paczki

- 24 października w historii kodu pojawiła się samodzielna wersja postaci Viliana z edytorem macek. Można było korygować ich kształt i oglądać postać poza rozgrywką.
- 29 października powstała paczka źródeł PHP, konfiguracja wdrożenia na Renderze oraz szkielet projektu Android z instrukcjami budowania. Wpisy z tego dnia dokumentują przygotowanie źródeł i procesu kompilacji.

## Rozgrywka 2.5D i przejście do scen 3D

- W 2.5D rozbudowałam poruszanie się na mackach, celowanie w ludzi i chwyt dłonią. Zdarzenia ataku dostały krótkie napisy i oprawę dźwiękową. W paczce są edytor map, chwytacz kafli, edytor macek oraz osobny edytor macki ataku.
- W 3D przeniosłam ruch w wielu kierunkach, kamerę śledzącą lub swobodną oraz atak, który wypuszcza dłoń, zaciska palce i przyciąga cel. Ludzie reagują na bohatera, uciekają i próbują omijać przeszkody. Domyślna skala sylwetki w 3D to około 48 pikseli projektowych bez macek.
- Do ulicy doszły większe etapy z przejściami w poprzek i port z nabrzeżem, statkiem, żurawiami oraz kontenerami. Do portu trafiły dostarczone grafiki budynków, pojazdów, przeszkód i nawierzchni. Aktualna paczka 3D ma sześć plansz wbudowanych. To Ulica w ruinach, Stacja paliw, Posterunek, Port przemysłowy, Dzielnica Neonów i Park Nadbrzeżny. Po złapaniu wszystkich osób gra proponuje kolejny etap.
- Osobno powstał prototyp dziecięcy „Łowca potworków” w 2D. Ma własne zasoby, sterowanie i minimapę.

## 16 listopada — wspólne plansze, ustawienia i fabuła

- Dzielnica Neonów i Park Nadbrzeżny korzystają ze wspólnego układu w 2.5D i 3D. Dodałam je z dostarczonych kafli i grafik. Menu obu trybów pozwala wybrać planszę i ustawić styl obrazu. Układ HUD można przesuwać i zapisywać osobno dla pionu i poziomu.
- Hologram i nawigacja trafiły również do 2.5D. W 3D wskazanie celu uruchamia marsz omijający przeszkody. Znacznik pokazuje cel, a opcja widoczności pozwala wyłączyć linię trasy. Przód mapy można dopasować do kamery lub kierunku postaci.
- Dopisałam intro fabuły portu z zamkniętym kontenerem, nagraniem z przyszłości i próbą ucieczki. Doszły sceny „Drzwi schronu”, „Latarka nad wodą” i „Ostatni na schodach”. W dwóch zadaniach ratunkowych Vilian pomaga Idze wyciągnąć ochroniarza z wody i przytrzymuje grodź dla stworzenia niosącego dziecko. Sceny są zapisane jako [tekst fabularny w README](README.md).

## 17–20 listopada — edycja macek, modele i Creator 3D

- Rozbudowałam edytor macek 3D o osobne zakładki końcówek dotykających ziemi i macki ataku. Można ustawić punkty podparcia, kształt, końcówkę i ruch. Profil ataku obejmuje miejsce wyjścia macki, jej łuk, zasięg i fazy chwytu. Edytor pozwala obejrzeć atak w spoczynku albo w animacji.
- W paczce 3D użyłam dostarczonych modeli bohatera i dłoni z archiwów `vilian1.zip` i `lapa.zip`. Zoptymalizowane modele zawierają tekstury do 1024 pikseli i są osadzone w grze. Styl łączy obrysy, cel-shading i pikselowy obraz. Osobne ustawienia sterują efektami całego obrazu oraz wyglądem energii psi macek. Jakość obrazu, cienie i limit klatek można ustawić na słabsze urządzenie.
- Creator 3D jest dostępny z menu gry. Pozwala wybrać i ustawić punkt startowy oraz ludzi, wstawić obiekty, zmieniać ich położenie, obrót i skalę, użyć własnych modeli GLB/glTF i tekstur oraz rozegrać swoją planszę. Zapis projektu z zasobami działa w przeglądarce i można go wyeksportować.
- Aktualne wydania przeglądarkowe mają samodzielne pliki HTML i pełną paczkę źródeł z zasobami. Do samodzielnej wersji 3D `build3d.py` dołącza silnik Three.js, style, skrypty, modele i tekstury, żeby uruchamiała się bez pobierania ich z internetu.

## 20 listopada — hologram w grze 3D, wybór planszy i napisy

- Usunęłam ramkę i tło minimapy. W grze widać przez nią scenę, a druga kamera pokazuje półprzezroczyste meshe przeszkód, siatkę i małą sylwetkę Viliana, która porusza się razem z nim. Nad ludźmi pojawiają się kontrastowe trójkąty z obrysem. Po złapaniu danej postaci jej znacznik znika.
- Przeciągnięcie palcem obraca i przechyla wyłącznie hologram. Gest dwoma palcami i suwak w ustawieniach przybliżają jego scenę do 400 procent. Uchwyt przesuwa hologram po ekranie, a przyciski zmieniają jego rozmiar. Suwak głównej kamery pozwala podejść bliżej sylwetki.
- Dotknięcie mapy domyślnie uruchamia marsz. W ustawieniach można wybrać natychmiastowy przeskok na wskazane wolne miejsce. Okno wyboru planszy można przesunąć za nagłówek. Hologram i przycisk wyboru planszy można osobno ukryć i przywrócić w ustawieniach HUD.
- Dodałam do 3D oryginalne kwestie z 2.5D. Podpisy odpowiadają między innymi pudłu, schwytaniu, szarpaniu się, krzykowi i zakończeniu chwytu. Ich widoczność można przełączyć osobno od dźwięku.
- Zweryfikowałam składnię skryptów oraz poprawność samodzielnego HTML i paczki ZIP. Testy logiki potwierdziły niezależny obrót mapy, przeliczenie dotknięcia po zmianie widoku, blokowanie przeskoku na przeszkodę, znikanie znacznika po złapaniu, oryginalny tekst podpisów i zapisywanie położenia okna plansz. Płynność oraz wygląd na fizycznym telefonie pozostają do zweryfikowania.

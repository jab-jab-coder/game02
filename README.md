# Pierogi na czas 🥟

Zręcznościowa gra dla dwóch osób na pady, do grania na jednym komputerze albo online z dwóch różnych miejsc. Wigilia u babci Halinki, goście przyjdą za 3 minuty, a w kuchni chaos. Ulepcie i podajcie jak najwięcej pierogów, zanim kot zje farsz, a wujek Zbyszek resztę.

## Uruchomienie

Otwórz `index.html` w przeglądarce (Chrome, Edge, Firefox). Nie trzeba nic instalować ani budować: gra to `index.html` plus biblioteka `peerjs.min.js`, wczytywana tylko w trybie online.

1. Podłącz dwa pady (USB lub Bluetooth) i naciśnij na każdym dowolny przycisk, żeby przeglądarka je wykryła.
2. Naciśnij **A** na padzie albo **Enter**.
3. Dwuklik na grze włącza pełny ekran.

Grę można też opublikować przez GitHub Pages (Settings → Pages → gałąź `main`), wtedy działa pod linkiem.

## Gra online (dwa komputery)

Gra musi być otwarta z adresu WWW (np. GitHub Pages), żeby druga osoba mogła wejść tym samym linkiem.

1. Pierwsza osoba (host) na ekranie tytułowym klika **Załóż pokój**. Pojawi się kod pokoju i link.
2. Host wysyła link drugiej osobie (przycisk **Kopiuj link**). Zamiast linku można wpisać sam kod w polu **KOD** i kliknąć **Dołącz**.
3. Gdy druga osoba dołączy, dowolne z Was naciska **A** lub **Enter** i runda rusza.

Host jest Graczem 1, osoba dołączająca Graczem 2. Każdy gra na swoim padzie (pierwszym wykrytym) albo na klawiaturze, przy czym online działają oba układy klawiszy naraz. W prawym dolnym rogu widać stan połączenia i ping.

Jak to działa i czego się spodziewać:

- Całą grę liczy przeglądarka hosta. Gość wysyła tylko swoje przyciski i około 30 razy na sekundę dostaje aktualny stan, więc swoje ruchy widzi z opóźnieniem równym pingowi.
- Połączenie jest bezpośrednie między przeglądarkami (WebRTC). Do samego zestawienia go służy darmowy publiczny serwer PeerJS, który nie daje gwarancji dostępności. Gdy nie działa, nie da się założyć pokoju ani dołączyć, ale gra lokalna działa normalnie.
- Przy niektórych routerach i sieciach firmowych połączenie bezpośrednie może się nie zestawić. Wtedy pomaga inna sieć (np. hotspot z telefonu).
- Karta z grą u hosta musi być otwarta i widoczna. Przeglądarki wstrzymują grę w karcie schowanej w tle, a gość widzi wtedy „Brak sygnału od hosta”.
- Jeśli gość straci połączenie, może wrócić tym samym linkiem, także w trakcie rundy. Jeśli host zamknie kartę, pokój znika i trzeba założyć nowy.
- Gra nie przenosi głosu, do rozmowy potrzebny jest osobny telefon lub komunikator.

Własny serwer pokoi (PeerServer) można wskazać parametrami adresu: `?peerhost=adres&peerport=443`.

## Sterowanie

| Akcja | Pad | Gracz 1 (klawiatura) | Gracz 2 (klawiatura) |
|---|---|---|---|
| Ruch | lewa gałka / krzyżak | W A S D | strzałki |
| Weź / odłóż / przegoń kota / podkradnij | A | F | K |
| Rzut (przytrzymaj, żeby ustawić siłę, puść, żeby rzucić) | X (lub B) | G | L |
| Lepienie (na zmianę) | LB / RB (lub LT / RT) | Q / E | I / O |

W grze lokalnej pierwszy wykryty pad steruje Graczem 1, drugi Graczem 2. Klawiatura działa równolegle, więc można grać też bez padów.

## Jak się gra

1. **Ciasto**: weź krążek ciasta.
2. **Farsz**: nałóż farsz warzywny.
3. **Stolnica**: ulep pieroga, wciskając na zmianę LB i RB.
4. **Garnek**: wrzuć pieroga (mieszczą się 3) i wyjmij, gdy pierścień jest zielony, a najlepiej złoty.
5. **Stół**: podaj.

Przedmioty można rzucać do partnera, który złapie je sam, jeśli ma wolne ręce. Przytrzymanie przycisku rzutu uruchamia wskaźnik siły, który chodzi tam i z powrotem. Im wyższa siła w chwili puszczenia, tym dalej poleci pieróg, a kółko na podłodze pokazuje, gdzie spadnie. W trakcie celowania chodzi się wolniej. Celny rzut surowym pierogiem do garnka też się liczy, a ugotowanym prosto na stół daje premię.

## Punktacja

| Zdarzenie | Punkty |
|---|---|
| Podany pieróg | +10 |
| Podany idealny pieróg (złoty pierścień) | +15 |
| Rzut ugotowanym pierogiem prosto na stół | dodatkowe +5 |
| 3 podania z rzędu bez wpadki | mnożnik x2 |
| 6 podań z rzędu bez wpadki | mnożnik x3 |
| Pieróg na podłodze | −5 |
| Rozgotowany pieróg | −5 |
| Kot siedzi przy farszu lub przy garnku (także z samą wodą) | −2 co sekundę, od chwili dojścia aż do przegonienia |
| Wujek Zbyszek zjadł pieroga z rąk | −10 |

Każda wpadka zeruje combo.

Wynik jest wspólny i to on decyduje o ocenie babci (od „Głodni pójdą…” do „MOJA KREW!”). Osobno liczony jest wkład każdego gracza: punkty dostaje ten, kto podał pieroga na stół. Kto ma większy wkład, zostaje „ulubionym wnukiem”, więc gotowego pieroga można partnerowi podkraść z rąk.

## Przeszkadzajki

- **Kot Mruczek** wchodzi górnymi drzwiami i idzie do farszu. Przegoń go przyciskiem A.
- **Kot Filemon** wchodzi tymi samymi drzwiami i idzie do garnka. Poza zabieraniem punktów co kilka sekund wyławia z niego pieroga. Przegania się go tak samo.
- **Trzeci kot** wchodzi tymi samymi drzwiami i chodzi na zmianę: raz do farszu, raz do garnka. Przegania się go tak samo.
- **Wujek Zbyszek** wchodzi dolnymi drzwiami i goni tego, kto niesie ugotowanego pieroga. Nie da się go przegonić, trzeba go omijać albo przerzucać pierogi nad nim.
- **Kipiący garnek**: naciśnij A przy garnku w ciągu kilku sekund, inaczej wszystko się rozgotuje.
- **Suczka Nora**: złocistoruda suczka z ciemnymi uszami, siwym pyskiem i białymi łapami wchodzi na początku rundy i kładzie się spać w jednym z przejść (między garnkiem a stołem, ciastem a farszem, farszem a stolnicą albo stolnicą a garnkiem). Nie da się przez nią przejść, trzeba ją obejść, za to rzucane pierogi przelatują nad nią. Co 60–90 sekund (czas jest losowany) wstaje i przenosi się w inne przejście.
- **Mąka na podłodze**: poślizg i chwilowa utrata kontroli. Upuszczone ciasto też zostawia plamę.

## Technologia

Czysty HTML + JavaScript: Canvas 2D, Gamepad API i Web Audio, bez kroku budowania. Tryb online używa WebRTC przez bibliotekę [PeerJS](https://peerjs.com/) 1.5.5 (licencja MIT), dołączoną do repozytorium jako `peerjs.min.js`.

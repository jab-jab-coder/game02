# Pierogi na czas 🥟

Zręcznościowa gra dla dwóch osób na pady. Wigilia u babci Halinki, goście przyjdą za 3 minuty, a w kuchni chaos. Ulepcie i podajcie jak najwięcej pierogów, zanim kot zje farsz, a wujek Zbyszek resztę.

## Uruchomienie

Otwórz `index.html` w przeglądarce (Chrome, Edge, Firefox). Nie trzeba nic instalować ani budować, cała gra to jeden plik.

1. Podłącz dwa pady (USB lub Bluetooth) i naciśnij na każdym dowolny przycisk, żeby przeglądarka je wykryła.
2. Naciśnij **A** na padzie albo **Enter**.
3. Dwuklik na grze włącza pełny ekran.

Grę można też opublikować przez GitHub Pages (Settings → Pages → gałąź `main`), wtedy działa pod linkiem.

## Sterowanie

| Akcja | Pad | Gracz 1 (klawiatura) | Gracz 2 (klawiatura) |
|---|---|---|---|
| Ruch | lewa gałka / krzyżak | W A S D | strzałki |
| Weź / odłóż / przegoń kota / podkradnij | A | F | K |
| Rzut (przytrzymaj, żeby ustawić siłę, puść, żeby rzucić) | X (lub B) | G | L |
| Lepienie (na zmianę) | LB / RB (lub LT / RT) | Q / E | I / O |

Pierwszy wykryty pad steruje Graczem 1, drugi Graczem 2. Klawiatura działa równolegle, więc można grać też bez padów.

## Jak się gra

1. **Ciasto**: weź krążek ciasta.
2. **Farsz**: nałóż farsz.
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
| Kot dobrał się do farszu | −10 (co kilka sekund, dopóki go nie przegonisz) |
| Drugi kot wyłowił pieroga z garnka | −10 (co kilka sekund, dopóki go nie przegonisz) |
| Wujek Zbyszek zjadł pieroga z rąk | −10 |

Każda wpadka zeruje combo.

Wynik jest wspólny i to on decyduje o ocenie babci (od „Głodni pójdą…” do „MOJA KREW!”). Osobno liczony jest wkład każdego gracza: punkty dostaje ten, kto podał pieroga na stół. Kto ma większy wkład, zostaje „ulubionym wnukiem”, więc gotowego pieroga można partnerowi podkraść z rąk.

## Przeszkadzajki

- **Kot Mruczek** wchodzi górnymi drzwiami i idzie do farszu. Przegoń go przyciskiem A.
- **Kot Filemon** wchodzi tymi samymi drzwiami i idzie do garnka, z którego wyławia pierogi. Przegania się go tak samo.
- **Wujek Zbyszek** wchodzi dolnymi drzwiami i goni tego, kto niesie ugotowanego pieroga. Nie da się go przegonić, trzeba go omijać albo przerzucać pierogi nad nim.
- **Kipiący garnek**: naciśnij A przy garnku w ciągu kilku sekund, inaczej wszystko się rozgotuje.
- **Mąka na podłodze**: poślizg i chwilowa utrata kontroli. Upuszczone ciasto też zostawia plamę.

## Technologia

Czysty HTML + JavaScript: Canvas 2D, Gamepad API i Web Audio. Bez zależności i bez kroku budowania.

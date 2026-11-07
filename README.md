# Trzustka — interaktywny atlas dla pacjenta

Prezentacja po polsku, przeznaczona do rozmowy lekarza z pacjentem. Zawiera autorski, uproszczony model edukacyjny 3D. Geometria modelu i treści medyczne wymagają zatwierdzenia przez lekarza przed użyciem z pacjentami.

## Funkcje

- Obrót, przybliżenie, wybór i podświetlenie struktur.
- Widok zewnętrzny, umowny przekrój i przezroczystość.
- Podpisy struktur oraz przełączana widoczność sąsiednich narządów.
- Powiększony schemat mikroskopowy komórek pęcherzykowych i wysp trzustkowych.
- Animacje trawienia, regulacji glukozy i blokady ujścia przez kamień żółciowy.
- Sześć osobnych scenariuszy chorób, porównanie ze zdrową trzustką oraz wybór lokalizacji guza.
- Układ dla komputera i tabletu oraz tryb pełnoekranowy.

## Uruchomienie lokalne

Wymagany Node.js 18 lub nowszy. Projekt nie wymaga instalacji zależności ani kompilacji.

```sh
node serve.cjs
```

Otwórz adres wypisany w terminalu: `http://127.0.0.1:4173`. Zakończ podgląd skrótem Ctrl+C.

Plik `index.html` korzysta z modułów JavaScript, dlatego źródłową wersję należy uruchamiać przez serwer HTTP, a nie przez dwukrotne kliknięcie tego pliku.

## Pliki

- `index.html` — układ prezentacji.
- `style.css` — wygląd i układ responsywny.
- `app.js` — obsługa prezentacji, schematy i animacje.
- `model.js` — geometria 3D, kamera, wybór struktur i scenariusze.
- `content.js` — polskie opisy medyczne i źródła.
- `vendor/` — lokalna kopia Three.js 0.170.0 i OrbitControls.

## Zakres i źródła

Model nie jest rekonstrukcją badania pacjenta ani zwalidowanym atlasem klinicznym. Przedstawia wybrane relacje anatomiczne i typowy wariant ujścia przewodów. Proporcje, średnice przewodów, kolory, tempo przepływu i zmiany chorobowe mają charakter schematyczny. Nie służy do rozpoznawania chorób na podstawie objawów ani do planowania leczenia.

Pełna lista źródeł i opis uproszczeń są dostępne w prezentacji w sekcji „Źródła i zakres modelu”. Treści oparto m.in. na materiałach Johns Hopkins, NIDDK, National Cancer Institute i Endocrine Society. Data sprawdzenia źródeł: 7 listopada 2026 r.

## Biblioteki

Three.js i OrbitControls są udostępnione na licencji MIT. Treść licencji znajduje się w `vendor/LICENSE.txt`. Ta licencja dotyczy biblioteki, a nie automatycznie całego projektu.

Prezentacja nie zbiera danych pacjentów i nie wymaga zewnętrznych usług do działania. Odnośniki do źródeł medycznych wymagają internetu.

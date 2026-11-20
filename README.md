# Zielski.info

Otwórz `index.html` w przeglądarce, aby sprawdzić stronę lokalnie.
Niebieska pigułka zostawia Cię nad chmurami i wyświetla krótki żart.
Kliknij czerwoną pigułkę, wpisz `matrix` i naciśnij Enter. Druga linijka
jest zapisana w Base64 jako easter egg. Każdy z dostępem do kodu strony
może ją odczytać.

## Publikacja na GitHub Pages

1. Rozpakuj ZIP. W istniejącym repozytorium strony sprawdź **Settings → Pages**,
   żeby znaleźć źródło publikacji. Zaktualizuj pliki właśnie w tym folderze
   i zachowaj istniejący plik `CNAME`, jeśli już wskazuje na zielski.info.
2. Przy nowej stronie na darmowym GitHubie utwórz publiczne repozytorium
   `zielski-info`. Przez **Add file → Upload files** wgraj `index.html`
   oraz `clouds.webp` z rozpakowanego folderu i zrób commit.
   Plik `.nojekyll` jest opcjonalny dla tego projektu. Możesz go wgrać przez Git
   lub przez **Add file → Create new file**, jeśli nie widzisz go po rozpakowaniu.
3. Dla nowego repozytorium wybierz **Settings → Pages → Deploy from a branch
   → main → / (root) → Save**. Po udanym wdrożeniu otwórz adres podany w Pages.

## Domena zielski.info

1. Jeśli podłączasz domenę po raz pierwszy, wejdź w ustawienia konta GitHub
   **Settings → Pages → Add a domain**. Dodaj rekord TXT o nazwie i wartości
   podanych przez GitHub, kliknij **Verify** i zachowaj rekord TXT.
2. Wejdź w **Settings → Pages** repozytorium, ustaw **Custom domain** na
   `zielski.info` i kliknij **Save**. GitHub zapisze plik `CNAME` w źródle
   publikacji przy publikacji z gałęzi. Jeśli domena jest już przypisana
   do właściwego repozytorium, sprawdź ustawienie bez dodawania jej od nowa.
3. U dostawcy DNS ustaw poniższe rekordy. Zastąp wyłącznie rekordy routujące,
   które kolidują dla `@` lub `www` (np. stare A lub AAAA). Zachowaj rekordy
   poczty i weryfikacji. Jeśli domena działa już na GitHub Pages z tymi
   rekordami, zostaw DNS bez zmian.

   | Typ | Nazwa | Wartość |
   | --- | --- | --- |
   | A | @ | 185.199.108.153 |
   | A | @ | 185.199.109.153 |
   | A | @ | 185.199.110.153 |
   | A | @ | 185.199.111.153 |
   | CNAME | www | TWOJ-LOGIN.github.io |

   Zastąp `TWOJ-LOGIN` nazwą właściciela repozytorium. Wartość CNAME
   wpisz bez https i bez ścieżki repozytorium.
4. Gdy kontrola DNS przejdzie i GitHub wystawi certyfikat, zaznacz
   **Enforce HTTPS**. Sprawdź `https://zielski.info` i `https://www.zielski.info`.
   GitHub podaje, że propagacja zmian DNS może potrwać do 24 godzin.

[Publikacja z gałęzi](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site) · [Weryfikacja domeny](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/verifying-your-custom-domain-for-github-pages) · [Konfiguracja DNS](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site)

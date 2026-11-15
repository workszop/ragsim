# ragsim

Symulator RAG krok po kroku (PL/EN), https://symulator-rag.warsztaty-ai.com/

Jeden plik `index.html`, bez kroku budowania. Styl: edulab (edustyl).

Osiem kroków w dwóch grupach:

- **Przygotowanie wiedzy:** dokument → podział na fragmenty po 3 zdania → baza wektorowa (12 liczb na fragment, pokazane jako słupki).
- **Pytanie i odpowiedź:** wybór pytania → wektor pytania → wyszukiwanie (podobieństwo cosinusowe, najwyżej 3 fragmenty z wynikiem ≥ 0,35) → prompt → odpowiedź ze źródłami.

Wektory są deterministyczne: 12 ukrytych tematów, słowa kluczowe dopasowane po początku wyrazu (działa z polską odmianą i znakami diakrytycznymi). Odpowiedź powstaje regułami tylko z fragmentów, które trafiły do promptu. Ostatnie pytanie celowo nie pasuje do dokumentu.

- Tryby: Notatnik (wszystkie przebyte kroki otwarte) i Prezentacja (większe litery, otwarty jeden krok; klik w pasek kroków otwiera wybrany). Na telefonie zawsze Notatnik.
- Klawisze: `→` / `Enter` dalej, `←` wstecz, `R` od nowa, `Alt+P` prezentacja.
- Dokument można edytować w kroku 1; zmieniony tekst zostaje po zmianie języka.
- `window.RAG` udostępnia stan i silnik do testów.

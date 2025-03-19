# Analiza przestrzenna dla przejazdów karetek w Małopolsce

**Opis problemu badawczego:** System ratownictwa medycznego odgrywa kluczową rolę w zapewnianiu szybkiej pomocy w nagłych wypadkach. Analiza tras przejazdów karetek pozwala na identyfikację wzorców czasowych i przestrzennych, ocenę efektywności dojazdów oraz wskazanie obszarów wymagających usprawnienia. Celem projektu jest eksploracyjna analiza przejazdów karetek w województwie małopolskim na podstawie danych GPS oraz badanie czynników wpływających na czas reakcji służb ratunkowych.

**Źródło danych** - od prowadzącego

**Proponowane techniki analizy danych:**

- Wstępna analiza danych GPS
    - Oczyszczenie i agregacja danych GPS dla poszczególnych kursów
    - Sprawdzenie kompletności danych (np. braki w sygnale, nieprawidłowe punkty)
- Analiza czasowa i przestrzenna przejazdów
    - Średnie czasy dojazdu do poszczególnych miejscowości / na poszczególnych obszarach / w siatce H3
    - Analiza godzin szczytu – czy w określonych porach dnia występują większe opóźnienia?
    - Wizualizacja gęstości przejazdów – heatmapy najczęściej uczęszczanych tras.
- Wykrywanie anomalii i problematycznych obszarów
    - Identyfikacja tras o nienaturalnie długich czasach przejazdu (np. korki, zła infrastruktura).
    - Wykrycie często omijanych obszarów – możliwe luki w pokryciu ratowniczym.
    - Analiza wpływu terenów zurbanizowanych vs wiejskich na efektywność dojazdu.
- ?Modelowanie predykcyjne czasu dojazdu?
    - Regresja liniowa/random forest – przewidywanie czasu przejazdu na podstawie odległości, godziny, warunków drogowych.
    - Modelowanie szeregów czasowych (ARIMA, Prophet) – przewidywanie natężenia przejazdów w przyszłych okresach.
    - Analiza sieciowa (graph analysis) – optymalizacja tras na podstawie danych OSM i sieci dróg.

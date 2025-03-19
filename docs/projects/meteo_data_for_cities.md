# Zmiany klimatyczne w miastach - analiza trendów w danych z Copernicus Climate Data Store

**Opis problemu badawczego:** Zmiany klimatu wpływają na warunki atmosferyczne w miastach, wzmacniając efekt miejskiej wyspy ciepła (UHI) i zmieniając wzorce opadów czy prędkości wiatru. Celem projektu jest analiza długoterminowych trendów wybranych parametrów meteorologicznych (np. temperatura, opady, prędkość wiatru) w wybranych aglomeracjach na podstawie wybranych źródeł danych. Badanie pozwoli określić tempo zmian oraz ich sezonowość, a także porównać miasta o różnych warunkach klimatycznych.

**Proponowane źródła danych:**

- [ERA-5 daily statistics - CDS](https://cds.climate.copernicus.eu/datasets/derived-era5-single-levels-daily-statistics?tab=overview)
- Inne, znalezione samodzielnie

**Dodatkowe informacje:**

- CDS posiada własne [API](https://cds.climate.copernicus.eu/how-to-api)
- ECMWF posiada własny projekt [earthkit](https://earthkit.readthedocs.io/en/latest/#), który niby (nie korzystałem z niego) ułatwia wczytywanie i pracę z danymi

**Proponowane techniki analizy danych:**

- Wstępne czyszczenie i agregacja danych szeregów czasowych (np. uśrednianie miesięczne lub roczne)
- Eksploracyjna analiza danych (EDA) - wykresy trendów w czasie, wykresy korelacji
- Analiza statystyczna trendu (np. dopasowanie liniowej regresji trendu lub krzywej nieliniowej)
- Modelowanie szeregów czasowych - zastosowanie modeli prognostycznych (np. ARIMA, Prophet lub LSTM) do przewidywania przyszłych wartości
- Ocena niepewności prognoz i walidacja modelu na danych historycznych (podział na zbiór treningowy i testowy z ostatnich lat)
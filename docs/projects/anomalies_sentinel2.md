# Wykrywanie anomalii na obrazach Sentinel-2

**Opis problemu badawczego:** Dane optyczne pozwalają na monitorowanie zmian w środowisku, ale detekcja nietypowych zdarzeń (anomalii) wymaga zaawansowanej analizy danych. Anomalie mogą obejmować wylesienia, susze, pożary, zmiany pokrycia terenu, zanieczyszczenia wód i anomalia w roślinności. Celem projektu jest opracowanie systemu automatycznego wykrywania anomalii na podstawie wskaźników spektralnych i metod uczenia maszynowego, w tym algorytmów nadzorowanych i nienadzorowanych.

**Proponowane źródła danych:**

- Microsoft Planetary Computer
- Earth Search by Element 84 (AWS Registry of Open Data)
- Google Earth Engine
- Copernicus Data Space Ecosystem

**Proponowane techniki analizy danych:**

- Wstępne przetwarzanie - korekcja atmosferyczna, maskowanie chmur, przycięcie do AOI
- Ekstrakcja cech spektralnych - obliczenie wskaźników spektralnych (np. NDVI czy MSAVI - zmiany wegetacji, NDWI - zmiany dot. zasięgu wód powierzchniowych, NBR - wykrywanie pożarów)
- Wykrywanie anomalii
    - Metody statystyczne (reguły odstające):
        - Z-score – oznaczanie wartości odległych od średniej o więcej niż X odchyleń standardowych
        - Percentylowa analiza progowa – wykrywanie wartości powyżej 95. lub poniżej 5. percentyla dla danego obszaru i wskaźnika spektralnego
        - Metody bazujące na głównych składowych (PCA) – analiza kierunków największej wariancji i identyfikacja punktów odstających
    - Metody wykrywania anomalii oparte na ML (unsupervised learning):
        - Isolation Forest – model izolujący nietypowe obserwacje (np. nagłe zmiany NDVI po wylesieniu).
        - Local Outlier Factor (LOF) – wykrywanie anomalii poprzez analizę gęstości punktów w przestrzeni cech spektralnych.
        - DBSCAN – grupowanie anomalii na podstawie gęstości obserwacji (pozwala wykrywać lokalne zmiany w środowisku).
        - Autoenkodery (AE) – redukcja wymiarowości i wykrywanie nietypowych pikseli poprzez różnicę między rekonstrukcją a rzeczywistym obrazem.
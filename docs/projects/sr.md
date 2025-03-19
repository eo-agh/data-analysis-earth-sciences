# Porównanie dostępnych modeli Super Resolution dla danych Sentinel-2

**Opis problemu badawczego:** Obrazy satelitarne Sentinel-2 oferują wielospektralne zobrazowania w różnych rozdzielczościach (10 m, 20 m, 60 m), ale nie wszystkie pasma mają wysoką rozdzielczość przestrzenną. To ogranicza ich wykorzystanie w precyzyjnych analizach środowiskowych, takich jak detekcja zmian, klasyfikacja pokrycia terenu czy monitoring urbanizacji. Celem projektu jest zastosowanie technik Super Resolution (SR) do poprawy jakości danych Sentinel-2, wykorzystując otwarte modele głębokiego uczenia do zwiększania rozdzielczości obrazów.

**Proponowane źródła danych:**

- W przypadku Sentinel-2 - Copernicus Data Space Ecosystem / Microsoft Planetary Computer / Earth Search by Element 84 (AWS Registry of Open Data)
- W przypadku modeli do SR:
    - DSen2
    - ESRGAN, SRCNN, HighResNet od AllenAI
    - Sentinel-2 Deep Resolution (S2DR2 / S2DR3)
    - Inne


**Proponowane techniki analizy danych:**

- Pobranie obrazów Sentinel-2
- Zastosowanie gotowych modeli
- Wizualne porównanie i analiza wybranego wskaźnika spektralnego
# Wykrywanie zmian wysokości terenu na podstawie danych SAR

**Opis problemu badawczego:** Zmiany wysokości terenu mogą być wynikiem zjawisk geologicznych (trzęsienia ziemi, wulkany, osuwiska), działań człowieka (eksploatacja górnicza, zapadliska, urbanizacja) lub procesów naturalnych (erozja, topnienie lodowców). Celem projektu jest monitorowanie przemieszczeń powierzchni ziemi w czasie, z wykorzystaniem danych SAR z różnych misji radarowych. Analiza będzie oparta na technikach interferometrycznych (InSAR).

**Proponowane źródła danych:**

- Sentinel-1 poprzez Copernicus Data Space Ecosystem / Microsoft Planetary Computer / Earth Search by Element 84 (AWS Registry of Open Data)
- Programy otwartych danych od komercyjnych dostawców (ICEYE, Umbra, Capella Space)

**Dodatkowe informacje:**

- Biblioteki dedykowane dla analiz na danych SAR to m.in. `PyGMTSAR` czy `MintPy`

**Proponowane techniki analizy danych:**

- Wybór analizowanego epizodu (np. [wulkan Fernandina - Galápagos Islands, Ecuador](https://mintpy.readthedocs.io/en/latest/demo_dataset/#sentinel-1_on_fernandina_with_isce2topsstack))
- Korekcja geometryczna i radiometryczna
- Tworzenie interferogramów – porównanie fazy fali radarowej
- Persistent Scatterer Interferometry (PS-InSAR) – analiza długoterminowych zmian wysokości
- Small Baseline Subset (SBAS) – krótkoterminowe zmiany
- Konwersja różnic fazowych na wartości wysokościowe
- Wizualizacja - mapy deformacji, wykresy zmian
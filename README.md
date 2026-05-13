# Spatiotemporal Signal Propagation Analysis

## Project Description
Projekt analizuje czasoprzestrzenną dynamikę propagacji sygnału ERK w populacjach komórek nabłonkowych. Wykorzystując dane z obrazowania pojedynczych komórek, badamy, w jaki sposób specyficzne mutacje onkogenne (PIK3CA, AKT1, PTEN) wpływają na wydajność komunikacji międzykomórkowej przy użyciu metryki ryzyka względnego (Relative Risk - RR) oraz analizy opóźnionej ekspozycji.

## Environment Setup
* **Wersja Python:** 3.12 lub nowsza.
* **Instalacja:** Zainstaluj wymagane zależności za pomocą poniższych komend:

# Instalacja pakietów
pip install -r requirements.txt

Step-by-Step ReproductionAby odtworzyć analizę i wygenerować wyniki dla Części A, uruchom poniższe notatniki Jupyter sekwencyjnie (możesz użyć "Run All" w VS Code/Jupyter):Task A1: Mutation Comparison * Plik: TaskA1_MutationComparison.ipynbOpis: Porównuje koordynację przestrzenną między linią dziką (WT) a mutantami przy użyciu testów statystycznych.Task A2: Lagged Exposure Analysis * Plik: TaskA2_LaggedExposure.ipynbOpis: Bada prędkość komunikacji poprzez przesunięcia czasowe ($\tau$) w celu znalezienia optymalnej skali czasowej ($\tau^*$).Task A3: Parameter Robustness Assessment * Plik: TaskA3_ParameterRobustness.ipynbOpis: Testuje czułość metryki RR względem promienia sąsiedztwa ($r$).Generated Output FilesPo uruchomieniu notatników, w folderze outputs/ pojawią się następujące pliki:ZadaniePlik WynikowyOpisA1mutations_comparison_table.csvStatystyki (mean RR, p-values) dla mutantów vs WT.A1mutation_comparison_plot.pngWykres słupkowy RR z błędami standardowymi.A2lagged_exposure_results.csvTabela z wartościami $\tau^*$ i max RR.A2lagged_exposure_plot.pngWykresy spadku RR w zależności od opóźnienia.A3parameter_sensitivity_results.csvDane z testów dla różnych promieni $r$.A3robustness_analysis_plot.pngWykres stabilności metryki RR.
# Porównanie klasyfikacji obrazów galaktyk z wykorzystaniem różnych architektur CNN <p style="text-align: center;">Część 2</p>
## 1. Wprowadzenie

Jest to kontynuacja pierwszego projektu o tej samej nazwie. Zmiana, którą wprowadziłem, jest wykorzystanie zdjęć galaktyk w rozmiarach 256 * 256. Jedna to wymusiło zupełnie inne podejście do problemów ze względu na sprzęt, którym dysponuje. W pierwszym artykule cały proces był wykonywany w jednym notebook, teraz ze względów wydajnościowych został podzielony na kilka etapów:
1. Przygotowanie danych
2. Uczenie modeli
3. Testowanie nauczonych modeli
4. Analiza otrzymanych wyników
## 2. Artykuł
Artykuł w przygotowaniu

## 3. Organizacja projektu
### 3.1. Przygotowanie danych
W notebook **CreateDate.ipynb** dane zostały podzielone na trzy części dane uczące, walidacyjne i testowe. Wygenerowałem również plik pdf, 
aby łatwiej można było zapoznać się z treścią notebook, nie uruchamiając całej inforatruktury potrzebnej do prawidłowego działania notebook.
### 3.2. Uczenie architektur
W projekcie został wykorzystany Jupiter Notebook dla wszystkich operacje. Jeden Notebook odpowiada jednej architekturze. Każdy Notebook zapisuje wyuczony model do pliku oraz informacje o procesie uczenia. Dzięki temu będzie możliwość wykorzystania tych plikóœ w przyszłości.
Notebooki zawierają następujące architektury:
- **DeepLearning.ipynb** — model głębokiej sieci neuronowej. W tym przypadku nie wykorzystuje architektur CNN.
- **ArchitectureLeNet5.ipynb** — jest to architektura przedstawiona przez Yann LeCun w 1989 roku.
- **ArchitectureAlexNet.ipynb** — AlexNet jest to architektura CNN z roku 2012. Została stworzona na zawody ImageNet Large Scale Visual Recognition Challenge (ILSVRC)
- **ArchitectureMobileNet.ipynb** — została zaprojektowana przez formę Google i jest przeznaczony na urządzenia mobilne.
- **ArchitectureVGG16.ipynb** — Zaprojektowana przez Visual Geomerty Group (VGG) na Uniwersytecie oksfordzkim. Charakteryzuje się prostotą i skutecznością, jednocześnie umożliwia naukę skomplikowanych hierarchicznych reprezentacji cech wizualnych. 
- **ArchitectureResNet50.ipynb** — Architektura powstała w 2015 roku. ResNet50 oznacza, że ma ona 50 warstw, ale są również modele z mniejszą liczbą warstw, takie jak ResNet-18, ResNet-32. Architektura jest nadal intensywnie wykorzystywany.
- **ArchitectureInception.ipynb** — Powstała w 2014 roku w firmie Google pod nazwą GoogLeNet. Później nazwa została zmieniona na Inception. Twórcy zastanawiali się, jak ulepszyć sieć jednocześnie nie tracąc na wydajności.
- **ArchitectureInceptionResNet.ipynb** — Połączenie dwóch sieci. Inception oraz ResNet. Dzięki zastosowaniu różnych splotów, tak jak w Inception, dodatkowo wprowadzono również bloki resztkowe tak jak w RestNet. 
- **ArchitectureXception.ipynb** — Pełna nazwa architektury to Extreme Inception. Powstał w 2017 roku jako ewolucja architektury Inception i został stworzony przez firmę Google. Architektura Xception okazała się bardziej wydajna od VGG-16, ResNet i Inception v3.
### 3.3. Przygotowanie wyników
W tej części przygotowano wyniki z każdej nauki. W skład wchodzą następujące Notebook:
- **Test.ipynb** — którego celem jest testowanie nauczonych modeli na podstawie danych testowych. Pozwala to również w późniejszym czasie na testowanie nowych obrazów.
- **Result.ipynb** — na postawie tego Notebook zostały przygotowane wykresy z wynikami testowania, umieszczone w artykule.
- **ResultMatrix.ipynb** — służy do tworzenia wykresów Matrix.
- **Learning.ipynb** — służy do przygotowania wykresów z danych otrzymanych podczas uczenia modeli.
## 4. Technologie
- Anaconda 23.11.0
- Python 3.10.13
- Jupyter notebook 7.0.6
## 5. Uruchomienie
Ja w swoim projekcie wykorzystuje Anaconda. Dobrze jest przy pomocy polecenia cd ustawić się w swoim katalogu projektu. Następnie wykonujemy następujące polecenia i Acaconda uruchamia się w przeglądarce.
```
conda activate [nazwa projektu w Anaconda]
jupyter notebook
````
Gdy chcemy zamknąć projekt, klikamy Ctrl + C, a następnie zgadzamy się i wykonujemy polecenie, aby wyłączyć środowisko, wykonujemy polecenie. 
```
conda deactivate
```


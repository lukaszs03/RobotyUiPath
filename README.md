# RobotyUiPath
 Wszystkie roboty jakie udało mi się do tej pory stworzyć - od najprostszych do bardziej zaawansowanych

## Pogodynka

![](images/main.png)


**1.GetCityName**

![](images/GetCityName.png)

Odpowiada za pobranie od użytkownika danych, w tym przypadku nazwy miasta, dla którego sprawdzana będzie pogoda.

**1.2 Write Line CityName**

Do sprawnego prowadzenia debugu :).

**2. Use Browser Edge: Google**

![](images/UseBrowserEdgeDO1.png)

Ta część odpowiada za zdefiniowanie adresu URL i pozostałych czynności.

***Do***
W tej części wybieram odpowiedni element przeglądarki przy użyciu *TypeInto* i ustawiam odpowiednie parametry, aby czynność była poprawna.

***Search, get, log***

![](images/SearchGetLog.png)

W tym miejscu za pomocą *Click, GetText, LogMessage* naprowadzam robota do wyszukania rekordu, pobrania i skopiowania temperatury ze wskazanego elementu, zapisania go do zmiennej oraz utworzenia logów do konsoli.

***GetTypeOfWeather, log***

![](images/gettypepluslog.png)

Następnie ponownie przy użyciu *GetText, LogMessage* pobieram dane dotyczące opisu pogody wraz z utworzeniem logu do konsoli.

**3. Analyze**

![](images/Analyze.png)

Ta sekcja odpowiada za logikę całej automatyzacji, na podstawie zapisanego kodu w *FlowDecision* kod stwierdza czy dana wartość jest *True* czy *False* i wybiera odpowiednią sugestie za pomocą *Assign* i zmiennej OutfitSuggestion.

**4. Display**

![](images/Dispaly.png)

Koniec, funkcja odpowiadająca za zwrócenie informacji użytkownikowi.

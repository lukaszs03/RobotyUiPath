# RobotyUiPath
 Portfolio prezentujące moje dotychczasowe projekty dotyczące automatyzacji RPA; zarowno prostsze prace jak i te bardziej zaawansowane
 Opis każdego robota znajduje się poniżej.

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

## DataCapturing
Automatyzacja na podstawie bazy danych Klientów *customers*, robot pobiera dane z pliku i następnie dodaje je w aplikacji webowej CRM (https://www.theautomationchallenge.com/crm) oraz desktopowej.

**1. Main**

![](images/dt_main.png)

Za pomocą *Parallel* łącze dwa workflows co pozwala na uruchomienie obu automatyzacji.

**2. WebDataCapturing**

![](images/dt_readusedo.png)

W tej części automatyzowana jest wersja webowa aplikacji, za pomocą *ReadRange* pobieram dane z pliku, następnie wybieram przeglądarke i ustanawiam URL. 
W dalszej części używam *ForEachRow* i tworzę zmienną.

![](images/dt_bodytype.png)

Używając *TypeInto* wskazuje miejsca, w jakie mają być wpisane poszczególne dane z bazy, wszystko konwertuje do *String* aby uniknąć błędu.

![](images/dt_ifgender.png)

Przy użyciu *If*, robot sprawdza, czy w kolumnie nr 2 "gender" jest słowo *Female*, na podstawie tego dokonuje wyboru i przy użyciu *Click* wybiera odpowiednią opcję.

![](images/dt_typestate.png)

Za pomocą kolejnych *TypeInto* i *SelectItem* wskazuję pola do wpisania prawidłowych danych oraz zajmuję się rozsuwaną listą.

![](images/dt_typeclicklog)

*TypeInto*, *Click*, *LogMessage* - kolejne miejsca do wpisania danych, na zakończenie robot finalizuje czynność dodając rekord do CRM i wysyła do logów poniższą informację.

![](images/dt_logoutput.png)

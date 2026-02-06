# Plan nauki — od Power BI Developera do eksperta automatyzacji i AI

> **Autor profilu**: Piotr Młynarz | Power BI Developer @ EY
> **Punkt startowy**: Power BI, DAX, SQL, Excel, Power Query
> **Cel docelowy**: Ekspert Power BI + automatyzacja procesów back office z elementami AI
> **Horyzont**: 12-18 miesięcy

---

## Zidentyfikowane luki kompetencyjne

| Luka | Poziom zagrożenia | Dlaczego to ważne |
|------|-------------------|-------------------|
| Brak programowania (Python) | KRYTYCZNY | Automatyzacja i AI opierają się na kodzie — low-code ma swoje granice |
| Minimalna znajomość Azure | WYSOKI | EY operuje w ekosystemie Microsoft — Azure to fundament infrastruktury |
| Brak umiejętności dokumentacji | WYSOKI | W konsultingu dokumentacja = produkt, klient za nią płaci |
| Git/DevOps na początku drogi | ŚREDNI | Praca zespołowa nad kodem wymaga wersjonowania i wspólnych procesów |
| Zależność od AI bez rozumienia fundamentów | STRATEGICZNY | Kopiowanie outputu AI bez zrozumienia tworzy kruche rozwiązania |

---

## FAZA 1: Fundamenty (miesiąc 1-3)

Cel fazy: zbudować bazę bez której dalsze kroki będą niestabilne.

---

### 1.1 Git i GitHub

**Dlaczego teraz**: każdy kolejny projekt nauki będzie repozytorium — im szybciej Git stanie się nawykiem, tym lepiej.

#### Krok 1 — Opanuj podstawowy cykl pracy
- `git init` — tworzenie repozytorium
- `git add` — dodawanie plików do śledzenia
- `git commit` — zapisywanie zmian z opisem
- `git push` / `git pull` — synchronizacja z GitHub
- `git status` i `git log` — orientacja co się dzieje w repozytorium

**Ćwiczenie**: Stwórz nowe repo na GitHubie o nazwie `python-nauka`. Każde ćwiczenie z Pythona (Faza 1.2) commituj i pushuj. Cel: minimum 30 commitów w pierwszym miesiącu.

#### Krok 2 — Branche i merge
- Tworzenie branchy (`git branch`, `git checkout -b`)
- Przełączanie się między branchami
- Merge — łączenie branchy
- Rozwiązywanie konfliktów merge

**Ćwiczenie**: W repozytorium `python-nauka` stwórz branch `eksperyment`, dodaj w nim nowy plik, a potem zmerguj go do `main` przez Pull Request na GitHubie.

#### Krok 3 — Współpraca przez GitHub
- Pull Requesty — tworzenie, opisywanie, review
- Issues — zgłaszanie zadań i błędów
- GitHub Pages — publikowanie stron (to już znasz)
- Pliki README.md — opis repozytorium (łączy się z nauką dokumentacji)

**Ćwiczenie**: Znajdź na GitHubie publiczne repozytorium z danymi (np. dataset), zrób fork, dodaj coś (np. analizę) i wyślij Pull Request.

#### Kamień milowy Gita
> Potrafisz samodzielnie: stworzyć repo, pracować na branchach, zrobić PR, rozwiązać konflikt merge, napisać README.md.

---

### 1.2 Python — podstawy przez pryzmat danych

**Dlaczego teraz**: Python to język nr 1 w danych, automatyzacji i AI. Nie musisz zostać programistą — musisz rozumieć kod na tyle, żeby go czytać, debugować i modyfikować.

**Narzędzia do zainstalowania**:
- VS Code (edytor kodu) + rozszerzenie Python
- Python 3.x (ze strony python.org lub przez Microsoft Store)
- Terminal / wiersz poleceń (do uruchamiania skryptów)

#### Krok 1 — Absolutne podstawy składni
- Zmienne i typy danych (string, int, float, bool)
- Operatory (matematyczne, porównania, logiczne)
- Wypisywanie wyników (`print()`)
- Komentarze w kodzie

**Ćwiczenie**: Napisz skrypt który oblicza ile dni zostało do końca roku i wypisuje wynik.

#### Krok 2 — Struktury danych
- Listy (`list`) — odpowiednik kolumny w tabeli
- Słowniki (`dict`) — odpowiednik wiersza z nagłówkami
- Zbiory (`set`) i krotki (`tuple`) — kiedy ich używać
- Indeksowanie i wycinanie (slicing)

**Ćwiczenie**: Stwórz listę 10 spółek z EMIS. Napisz kod który filtruje te z przychodem powyżej zadanej wartości (dane zapisane jako lista słowników).

#### Krok 3 — Instrukcje warunkowe i pętle
- `if`, `elif`, `else` — podejmowanie decyzji
- `for` — iteracja po listach i zakresach
- `while` — pętle z warunkiem
- `break` i `continue` — kontrola pętli
- List comprehension — skrócony zapis pętli (bardzo pythonowy wzorzec)

**Ćwiczenie**: Masz listę 20 spółek ze statusem (aktywna/nieaktywna). Napisz pętlę która wypisuje tylko aktywne i liczy ile ich jest.

#### Krok 4 — Funkcje
- Definiowanie funkcji (`def`)
- Parametry i wartości domyślne
- Zwracanie wyników (`return`)
- Dlaczego funkcje są ważne (reużywalność, czytelność)

**Ćwiczenie**: Napisz funkcję `czy_duza_spolka(przychod, prog=1000000)` która zwraca `True` jeśli przychód przekracza próg. Użyj jej w pętli do filtrowania listy spółek.

#### Krok 5 — Praca z plikami
- Otwieranie i czytanie plików tekstowych
- Zapis do plików
- Format CSV — czytanie i zapis bez bibliotek
- Format JSON — podstawy (ważne dla API i Power Automate)

**Ćwiczenie**: Wyeksportuj dane z Power BI do CSV. Napisz skrypt Python który wczytuje ten plik, przetwarza dane i zapisuje wynik do nowego CSV.

#### Krok 6 — Biblioteka pandas (odpowiednik Power Query)
- Instalacja bibliotek (`pip install pandas`)
- Wczytywanie danych: `pd.read_csv()`, `pd.read_excel()`
- DataFrame — odpowiednik tabeli
- Filtrowanie wierszy, wybieranie kolumn
- Grupowanie (`groupby`) — odpowiednik Group By w Power Query
- Łączenie tabel (`merge`) — odpowiednik Merge Queries
- Tworzenie nowych kolumn
- Eksport wyników

**Ćwiczenie kluczowe**: Weź transformację którą robisz w Power Query w pracy. Odtwórz ją krok po kroku w pandas. Porównaj wyniki — powinny być identyczne. To ćwiczenie łączy Twój mocny punkt (Power Query) z nowym narzędziem (Python).

#### Krok 7 — Obsługa błędów
- `try` / `except` — łapanie błędów zamiast crashowania
- Typowe błędy: `FileNotFoundError`, `KeyError`, `TypeError`, `ValueError`
- Kiedy obsługiwać błędy, a kiedy pozwolić programowi się zatrzymać

**Ćwiczenie**: Rozszerz skrypt z kroku 6 — dodaj obsługę sytuacji gdy plik CSV nie istnieje lub ma nieoczekiwane kolumny.

#### Krok 8 — Praca z API (fundament dla automatyzacji)
- Co to jest API i REST (analogia: API to kelner między Tobą a kuchnią)
- Biblioteka `requests` — wysyłanie zapytań HTTP
- Metody: GET (pobierz dane), POST (wyślij dane)
- Formaty odpowiedzi: JSON
- Kody statusu: 200 (ok), 404 (nie znaleziono), 401 (brak autoryzacji)

**Ćwiczenie**: Użyj darmowego API (np. dane o pogodzie lub kursach walut) — pobierz dane, przetwórz je w pandas i zapisz do CSV.

#### Kamień milowy Pythona
> Potrafisz: napisać skrypt od zera, wczytać CSV/Excel, przetworzyć dane w pandas, zapisać wynik, obsłużyć błędy, pobrać dane z API. Rozumiesz kod na tyle, że potrafisz przeczytać skrypt wygenerowany przez AI i ocenić czy robi to co powinien.

---

### 1.3 Dokumentacja techniczna

**Dlaczego teraz**: od Fazy 1 każdy projekt powinien mieć dokumentację — budujesz nawyk od razu.

#### Krok 1 — Markdown jako format bazowy
- Nagłówki (`#`, `##`, `###`)
- Listy (numerowane i punktowe)
- Pogrubienie, kursywa, kod inline
- Bloki kodu z oznaczeniem języka
- Tabele
- Linki i obrazki

**Ćwiczenie**: Napisz README.md dla repozytorium `python-nauka` w którym opisujesz czego się uczysz i co zawiera każdy plik.

#### Krok 2 — Struktura dobrej dokumentacji projektu
- **Co to jest** — jedna zdaniowa odpowiedź
- **Jak uruchomić** — krok po kroku, zakładaj że czytelnik nie zna projektu
- **Co robi** — opis funkcjonalności
- **Struktura plików** — co jest gdzie
- **Znane ograniczenia** — czego nie robi, co wymaga poprawy

#### Krok 3 — Dokumentacja procesów (ważne w EY)
- Diagramy procesów w Markdown (Mermaid — obsługiwany przez GitHub)
- Opis kroków procesu: wejście → przetwarzanie → wyjście
- Dokumentacja decyzji: dlaczego wybrano rozwiązanie A zamiast B

**Ćwiczenie**: Weź proces który automatyzujesz w pracy (np. generowanie raportu). Opisz go w Markdown: kto go inicjuje, jakie dane wchodzą, co się dzieje krok po kroku, co wychodzi na końcu.

#### Krok 4 — Korzystanie z AI do dokumentacji (ale z głową)
- Użyj AI do wygenerowania pierwszego draftu
- Zawsze przeczytaj i edytuj — AI nie zna kontekstu biznesowego
- Dodaj to czego AI nie wie: dlaczego podjęto daną decyzję, kto jest odbiorcą, jakie są ograniczenia

#### Kamień milowy dokumentacji
> Każdy Twój projekt na GitHubie ma README.md. Potrafisz opisać proces biznesowy w Markdown. Masz swój szablon dokumentacji którego używasz powtarzalnie.

---

## FAZA 2: Power Platform rozszerzony (miesiąc 3-6)

Cel fazy: stać się operacyjnym członkiem nowego teamu automatyzacyjnego.

---

### 2.1 Power Automate — od prostych do złożonych flow

#### Krok 1 — Trigery i podstawowe akcje
- Trigery czasowe (cykliczne uruchamianie)
- Trigery zdarzeniowe (nowy mail, nowy plik, zmiana w SharePoint)
- Podstawowe akcje: wyślij maila, utwórz plik, wyślij powiadomienie
- Zmienne w flow — tworzenie, przypisywanie, użycie

**Ćwiczenie**: Stwórz flow który codziennie o 9:00 wysyła Ci maila z przypomnieniem o zadaniach (treść pobrana z listy SharePoint).

#### Krok 2 — Warunki i pętle
- Condition (if/else w flow)
- Apply to each (pętla po elementach)
- Switch (wiele warunków)
- Do until (pętla z warunkiem stopu)

**Ćwiczenie**: Flow który sprawdza listę zadań w SharePoint — jeśli zadanie ma status "pilne" i jest nieprzypisane, wysyła powiadomienie do managera.

#### Krok 3 — Expressions (odpowiednik DAX/formuł)
- Funkcje tekstowe: `concat()`, `substring()`, `replace()`
- Funkcje daty: `utcNow()`, `addDays()`, `formatDateTime()`
- Funkcje logiczne: `if()`, `and()`, `or()`, `equals()`
- Funkcje kolekcji: `length()`, `first()`, `last()`
- Odwoływanie się do dynamicznej zawartości w expressions

**Ćwiczenie**: Stwórz flow który pobiera datę z formularza, oblicza ile dni do tej daty i w zależności od wyniku (mniej niż 7 dni vs więcej) wysyła różne wiadomości.

#### Krok 4 — Integracje z ekosystemem Microsoft
- SharePoint: tworzenie/edycja elementów list, zarządzanie plikami
- Excel Online: odczyt/zapis wierszy w tabelach
- Outlook: parsowanie maili, zarządzanie kalendarzem
- Teams: wysyłanie wiadomości, tworzenie kanałów
- OneDrive: operacje na plikach

**Ćwiczenie**: Flow który monitoruje folder w SharePoint — gdy pojawi się nowy plik Excel, odczytuje z niego dane, dodaje je do listy SharePoint i wysyła podsumowanie na Teams.

#### Krok 5 — Approval flows (bardzo ważne dla back office)
- Start and wait for an approval
- Typy: Approve/Reject, Custom Responses
- Sekwencyjne vs równoległe zatwierdzenia
- Timeout i eskalacja

**Ćwiczenie**: Stwórz proces zatwierdzania urlopu — pracownik wypełnia formularz, manager dostaje approval request, po zatwierdzeniu kalendarz się aktualizuje i HR dostaje powiadomienie.

#### Krok 6 — Obsługa błędów w flow
- Configure Run After (uruchom po błędzie)
- Scope (grupowanie akcji — odpowiednik try/catch)
- Wysyłanie alertów gdy flow się nie powiedzie
- Logowanie błędów do SharePoint/Excel

**Ćwiczenie**: Weź dowolny flow z powyższych kroków i dodaj obsługę błędów — jeśli cokolwiek się nie uda, flow wysyła Ci maila z opisem co poszło nie tak.

#### Krok 7 — Zaawansowane wzorce
- Child flows (wywoływanie flow z innego flow)
- HTTP connector (wywoływanie zewnętrznych API)
- Parse JSON (przetwarzanie odpowiedzi API)
- Parallel branches (równoległe wykonywanie akcji)
- Pagination i limity (praca z dużymi zbiorami danych)

**Ćwiczenie**: Stwórz flow który pobiera dane z zewnętrznego API (np. kursy walut NBP — darmowe API), parsuje JSON i zapisuje wynik do Excel Online.

#### Kamień milowy Power Automate
> Potrafisz samodzielnie zbudować wielokrokowy flow z warunkami, pętlami, approval, integracją z SharePoint/Teams/Excel, obsługą błędów i wywołaniem API.

---

### 2.2 Power Apps — budowanie aplikacji dla back office

#### Krok 1 — Canvas App od zera
- Tworzenie nowej Canvas App
- Ekrany, nawigacja między ekranami
- Kontrolki: etykiety, pola tekstowe, przyciski, galerie, formularze
- Właściwości kontrolek (Text, Color, Visible, OnSelect)

**Ćwiczenie**: Stwórz aplikację z dwoma ekranami — ekran powitalny z przyciskiem "Dalej" który przenosi na drugi ekran.

#### Krok 2 — Połączenie ze źródłem danych
- SharePoint List jako backend
- Excel Online jako źródło danych
- Dataverse (wprowadzenie — szczegóły w 2.3)
- Odczyt danych: `Gallery` + źródło danych
- Zapis danych: `SubmitForm()`, `Patch()`

**Ćwiczenie**: Stwórz listę SharePoint "Zgłoszenia" (tytuł, opis, status, data). Zbuduj aplikację z galerią wyświetlającą zgłoszenia i formularzem do dodawania nowych.

#### Krok 3 — Formuły Power Fx (język Power Apps)
- `Filter()` — filtrowanie danych (jak WHERE w SQL)
- `Sort()`, `SortByColumns()` — sortowanie
- `Search()` — wyszukiwanie tekstu
- `LookUp()` — znajdowanie pojedynczego rekordu
- `CountRows()`, `Sum()`, `Average()` — agregacje
- `Navigate()`, `Back()` — nawigacja
- `Set()`, `UpdateContext()` — zmienne

**Ćwiczenie**: Dodaj do aplikacji z kroku 2: pole wyszukiwania, filtr po statusie (dropdown) i licznik zgłoszeń.

#### Krok 4 — Formularze i walidacja
- EditForm, DisplayForm, NewForm
- Walidacja pól (wymagane, format, zakres)
- Wyświetlanie komunikatów o błędach
- Blokowanie przycisku submit gdy formularz jest niepoprawny

**Ćwiczenie**: Rozbuduj formularz zgłoszeń — dodaj walidację: tytuł min. 5 znaków, opis wymagany, data nie może być z przeszłości.

#### Krok 5 — Integracja z Power Automate
- Wywoływanie flow z Power Apps (przyciskiem)
- Przekazywanie parametrów do flow
- Odbieranie wyników z flow

**Ćwiczenie**: Po dodaniu zgłoszenia w aplikacji, uruchom flow który wysyła powiadomienie na Teams z danymi zgłoszenia.

#### Kamień milowy Power Apps
> Potrafisz zbudować działającą aplikację z formularzem, galerią, filtrowaniem, walidacją i integracją z Power Automate. Osoby z back office mogą z niej korzystać na telefonie i komputerze.

---

### 2.3 Dataverse — warstwa danych Power Platform

#### Krok 1 — Czym jest Dataverse i kiedy go używać
- Dataverse vs SharePoint List vs Excel — porównanie i kiedy co wybrać
- Środowiska (environments) w Power Platform
- Tabele standardowe vs niestandardowe (custom)

#### Krok 2 — Tworzenie tabel i kolumn
- Typy kolumn: tekst, liczba, data, wybór (choice), lookup, waluta
- Klucze główne i alternatywne
- Relacje między tabelami (1:N, N:N)
- Widoki (views) — predefiniowane filtry danych
- Formularze — konfiguracja bez kodu

**Ćwiczenie**: Zaprojektuj i stwórz w Dataverse model danych dla systemu zgłoszeń: tabela Zgłoszenia, tabela Kategorie (lookup), tabela Komentarze (relacja 1:N).

#### Krok 3 — Bezpieczeństwo danych
- Role bezpieczeństwa (Security Roles)
- Business Units
- Uprawnienia na poziomie tabeli: Create, Read, Update, Delete
- Udostępnianie rekordów (Sharing)

#### Krok 4 — Dataverse jako hub danych
- Podłączenie Dataverse do Power BI (DirectQuery vs Import)
- Podłączenie Dataverse do Power Apps
- Podłączenie Dataverse do Power Automate
- Jedna baza danych → wiele aplikacji i raportów

**Ćwiczenie**: Podłącz tabele z kroku 2 jednocześnie do: Power Apps (aplikacja do zarządzania), Power BI (dashboard ze statystykami), Power Automate (powiadomienia o nowych zgłoszeniach).

#### Kamień milowy Dataverse
> Rozumiesz kiedy użyć Dataverse zamiast SharePoint/Excel. Potrafisz zaprojektować model danych, ustawić relacje i podłączyć go do Power BI, Power Apps i Power Automate jednocześnie.

---

## FAZA 3: Azure i chmura (miesiąc 6-9)

Cel fazy: rozumieć infrastrukturę Microsoftu na której stoi Twoja praca i praca Twojego teamu.

---

### 3.1 Azure Fundamentals (AZ-900)

#### Dlaczego ten certyfikat
- Daje wspólny język z zespołem technicznym
- W EY certyfikaty Microsoft są cenione — zapytaj managera o refundację
- Materiały są darmowe na Microsoft Learn
- Egzamin nie wymaga umiejętności programowania

#### Kluczowe tematy do opanowania
- **Cloud concepts**: IaaS, PaaS, SaaS — czym się różnią
- **Azure architecture**: regiony, strefy dostępności, grupy zasobów, subskrypcje
- **Compute**: Virtual Machines, App Service, Azure Functions (serverless)
- **Storage**: Blob Storage, File Storage, Table Storage
- **Networking**: Virtual Network, Load Balancer (podstawy)
- **Identity**: Azure Active Directory (Entra ID), uwierzytelnianie, autoryzacja
- **Governance**: Policy, RBAC, Cost Management
- **Monitoring**: Azure Monitor, Log Analytics

**Ćwiczenie**: Załóż darmowe konto Azure (Azure Free Account — 200$ kredytu na 30 dni + 12 miesięcy wybranych usług za darmo). Przejdź moduły na Microsoft Learn dla AZ-900.

#### Kamień milowy AZ-900
> Zdany egzamin AZ-900. Rozumiesz podstawową architekturę Azure i potrafisz rozmawiać z zespołem o usługach chmurowych.

---

### 3.2 Azure dla Power Platform i danych

#### Krok 1 — Azure Logic Apps
- Logic Apps vs Power Automate — co je łączy i różni
- Kiedy wybrać Logic Apps zamiast Power Automate (skala, złożoność, integracje)
- Tworzenie flow w Logic Apps Designer
- Connectors i Custom Connectors

**Ćwiczenie**: Weź flow z Power Automate (Faza 2) i odtwórz go w Logic Apps. Porównaj: co jest łatwiejsze, co daje więcej możliwości.

#### Krok 2 — Azure Functions
- Co to serverless i dlaczego to ważne
- Tworzenie prostej funkcji w Pythonie
- Trigery: HTTP, Timer, Queue, Blob
- Integracja z Power Automate (HTTP connector → Azure Function)

**Ćwiczenie**: Stwórz Azure Function w Pythonie która przyjmuje listę liczb przez HTTP i zwraca ich sumę i średnią. Wywołaj ją z Power Automate.

#### Krok 3 — Azure Data Factory (ADF)
- ETL/ELT w chmurze — odpowiednik Power Query ale na skalę enterprise
- Pipeline, Activity, Dataset, Linked Service
- Kopiowanie danych między źródłami
- Harmonogramowanie (scheduling)

**Ćwiczenie**: Stwórz pipeline w ADF który kopiuje dane z pliku CSV w Blob Storage do bazy SQL w Azure.

#### Krok 4 — Azure SQL Database
- SQL w chmurze — rozszerzenie Twoich obecnych umiejętności SQL
- Tworzenie bazy, tabel, zapytań (składnia identyczna jak znasz)
- Połączenie z Power BI (DirectQuery)
- Bezpieczeństwo: firewall, użytkownicy, role

**Ćwiczenie**: Stwórz bazę Azure SQL, zaimportuj dane z CSV, podłącz do Power BI i zbuduj raport. Cały pipeline: plik → Azure SQL → Power BI.

#### Kamień milowy Azure
> Potrafisz uruchomić Azure Function, stworzyć pipeline w Data Factory i podłączyć Azure SQL do Power BI. Rozumiesz kiedy użyć Azure zamiast Power Platform.

---

## FAZA 4: AI i automatyzacja inteligentna (miesiąc 9-12)

Cel fazy: włączyć sztuczną inteligencję do rozwiązań automatyzacyjnych budowanych dla back office.

---

### 4.1 AI Builder w Power Platform

#### Krok 1 — Gotowe modele AI (prebuilt)
- **Document Processing**: ekstrakcja danych z faktur, formularzy, paragonów
- **Text Recognition (OCR)**: odczyt tekstu z obrazów i skanów
- **Sentiment Analysis**: analiza nastroju tekstu (pozytywny/negatywny/neutralny)
- **Key Phrase Extraction**: wyciąganie kluczowych fraz z tekstu
- **Language Detection**: rozpoznawanie języka
- **Business Card Reader**: odczyt danych z wizytówek

**Ćwiczenie**: Stwórz flow w Power Automate który monitoruje folder SharePoint — gdy pojawi się skan faktury (PDF/zdjęcie), AI Builder odczytuje dane (numer, kwota, data, sprzedawca) i zapisuje je do listy SharePoint.

#### Krok 2 — Trenowanie własnych modeli
- **Custom Document Processing**: nauczenie AI rozpoznawania Twoich specyficznych dokumentów
- **Classification**: kategoryzowanie tekstu do zdefiniowanych grup
- **Object Detection**: rozpoznawanie obiektów na zdjęciach
- Proces: zbieranie danych treningowych → tagowanie → trenowanie → testowanie → publikacja

**Ćwiczenie**: Zbierz 10-15 przykładów dokumentu który często przetwarzasz w pracy (np. raporty klientów w podobnym formacie). Wytrenuj model AI Builder do automatycznej ekstrakcji kluczowych pól.

#### Krok 3 — AI Builder + Power Apps
- Dodawanie komponentów AI do aplikacji Canvas
- Skanowanie dokumentów z poziomu aplikacji mobilnej
- Wyświetlanie wyników analizy AI w aplikacji

**Ćwiczenie**: Rozbuduj aplikację zgłoszeń z Fazy 2 — dodaj możliwość zrobienia zdjęcia dokumentu telefonem, AI Builder odczytuje tekst i automatycznie wypełnia pola formularza.

#### Kamień milowy AI Builder
> Potrafisz zintegrować AI Builder z Power Automate i Power Apps. Umiesz wybrać odpowiedni gotowy model lub wytrenować własny do specyficznych dokumentów.

---

### 4.2 Copilot Studio (dawniej Power Virtual Agents)

#### Krok 1 — Tworzenie podstawowego chatbota
- Tematy (Topics) — co bot rozumie i jak reaguje
- Trigery — frazy uruchamiające temat
- Węzły konwersacji: pytanie, warunek, wiadomość, akcja
- Testowanie bota w wbudowanym emulatorze

**Ćwiczenie**: Stwórz bota "FAQ Back Office" który odpowiada na 5 najczęstszych pytań osób z Twojego zespołu (np. "jak złożyć urlop", "gdzie jest szablon raportu").

#### Krok 2 — Integracja z danymi firmowymi
- Podłączenie do SharePoint (bot odpowiada na podstawie danych z list)
- Podłączenie do Dataverse
- Wywoływanie Power Automate z bota (np. bot tworzy zgłoszenie)
- Generative AI w Copilot Studio — bot odpowiada na podstawie dokumentów

**Ćwiczenie**: Rozbuduj bota FAQ — podłącz go do listy SharePoint z procedurami. Bot wyszukuje odpowiednią procedurę i wyświetla ją użytkownikowi.

#### Krok 3 — Publikacja i kanały
- Publikacja na Teams (najważniejszy kanał w EY)
- Osadzenie na stronie SharePoint
- Analityka: ile rozmów, jakie pytania, gdzie bot nie wiedział odpowiedzi

**Ćwiczenie**: Opublikuj bota FAQ na kanale Teams Twojego zespołu. Zbieraj feedback przez tydzień i popraw tematy które bot obsługuje słabo.

#### Kamień milowy Copilot Studio
> Masz działającego chatbota na Teams który odpowiada na pytania pracowników back office, korzysta z danych SharePoint i uruchamia flow Power Automate.

---

### 4.3 Podstawy systemów agentycznych

#### Krok 1 — Zrozumienie konceptów
- Co to jest agent AI (program który podejmuje decyzje i wykonuje akcje)
- Różnica między chatbotem a agentem (chatbot odpowiada, agent działa)
- Składniki agenta: cel, narzędzia (tools), pamięć, kontekst, reasoning
- Przykład: Claude Code którego teraz używasz — to agent z dostępem do narzędzi

#### Krok 2 — Agenci w ekosystemie Microsoft
- Copilot agents w Microsoft 365
- Autonomous agents w Copilot Studio
- Azure AI Agent Service
- Jak agenci łączą się z Power Platform (flow jako narzędzia agenta)

#### Krok 3 — Projektowanie procesów agentycznych
- Identyfikacja procesów które nadają się do agentyzacji
- Kryteria: powtarzalność, jasne reguły decyzyjne, dostęp do danych, mierzalny wynik
- Mapowanie: wejście → decyzje → akcje → wyjście
- Bezpieczeństwo: human-in-the-loop (człowiek zatwierdza kluczowe decyzje)

**Ćwiczenie**: Zidentyfikuj 3 procesy w Twoim back office które mogłyby być obsługiwane przez agenta. Dla każdego opisz: jaki cel ma agent, jakich narzędzi potrzebuje, gdzie wymaga ludzkiego zatwierdzenia.

#### Kamień milowy systemów agentycznych
> Rozumiesz czym agent AI różni się od chatbota i automatyzacji. Potrafisz zaprojektować proces agentyczny z uwzględnieniem narzędzi, decyzji i bezpieczeństwa.

---

## FAZA 5: Pozycjonowanie jako ekspert (miesiąc 12+)

Cel fazy: połączyć wszystkie umiejętności w unikatową kompetencję na rynku.

---

### 5.1 Twoja docelowa unikalna wartość

> **"Rozumiem dane (Power BI / SQL), potrafię automatyzować procesy (Power Platform / Azure) i wiem jak włączyć AI — a to wszystko w kontekście back office dużej organizacji."**

Takich ludzi jest bardzo mało. Większość specjalistów zna tylko jedną warstwę:
- BI Developer → robi raporty, ale nie automatyzuje
- Power Platform Developer → automatyzuje, ale nie rozumie danych
- AI Specialist → zna modele, ale nie rozumie procesów biznesowych

Ty łączysz wszystkie trzy + znasz kontekst klienta wewnętrznego w Big Four.

### 5.2 Portfolio i widoczność
- GitHub: repozytorium z projektami z każdej fazy
- LinkedIn: regularne posty o tym czego się uczysz (budowanie marki osobistej)
- Wewnętrzne prezentacje w EY: pokaż co zbudowałeś, naucz innych
- Certyfikaty: AZ-900, PL-900 (Power Platform Fundamentals), PL-200 (Power Platform Functional Consultant)

### 5.3 Rekomendowane certyfikaty Microsoft (kolejność)

| Kolejność | Certyfikat | Poziom | Co pokrywa |
|-----------|-----------|--------|------------|
| 1 | PL-900 | Fundamentals | Power Platform — przegląd całości |
| 2 | AZ-900 | Fundamentals | Azure — przegląd chmury |
| 3 | PL-200 | Associate | Power Platform Functional Consultant |
| 4 | PL-400 | Associate | Power Platform Developer (bardziej techniczny) |
| 5 | AI-900 | Fundamentals | Azure AI — przegląd usług AI |
| 6 | DP-900 | Fundamentals | Azure Data — przegląd usług danych |

---

## Podsumowanie faz

| Faza | Okres | Kluczowe umiejętności | Kamień milowy |
|------|-------|----------------------|---------------|
| 1 | Miesiąc 1-3 | Git, Python (pandas), dokumentacja | Samodzielne skrypty, README do każdego projektu |
| 2 | Miesiąc 3-6 | Power Automate, Power Apps, Dataverse | Działająca aplikacja + automatyzacja dla back office |
| 3 | Miesiąc 6-9 | Azure (AZ-900), Logic Apps, Functions, ADF | Certyfikat AZ-900, pipeline danych w chmurze |
| 4 | Miesiąc 9-12 | AI Builder, Copilot Studio, systemy agentyczne | Chatbot na Teams, automatyzacja z AI |
| 5 | Miesiąc 12+ | Integracja wszystkiego, certyfikaty, portfolio | Unikalna pozycja eksperta |

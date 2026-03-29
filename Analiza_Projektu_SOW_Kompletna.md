# Analiza projektu i wycena SOW: Mobilna tablica ogłoszeń
**Autor:** Nastka Dąbrowska

---

## Kontekst zadania

Analiza przeprowadzona dla projektu mobilnego realizowanego przez software house dla klienta zewnętrznego. Zadanie: ocena stanu projektu na podstawie harmonogramu i planu zasobów, analiza wymagań klienta oraz przygotowanie uproszczonego SOW z szacunkiem pracochłonności.

*Dane wejściowe zostały zanonimizowane (nazwy projektu i firmy zmienione), wolumen i struktura danych pozostały bez zmian.*

---

## Dane wejściowe

### Załącznik 1: Harmonogram projektu (stan na dzień analizy)

| WBS | Nazwa | Start | Koniec | Pracochłonność | Czas trwania | % ukończenia | Przypisany | Zależności |
|-----|-------|-------|--------|---------------|--------------|--------------|------------|------------|
| 1 | Projekt | D+0 | D+29 | 562h | 28.88d | 10% | | |
| 1.1 | Sprawy formalne | D+0 | D+9 | 29h | 8.00d | 91% | | |
| 1.1.1 | Uzgodnienie umowy | D+0 | D+2 | 24h | 3.00d | 100% | Prawnik | |
| 1.1.2 | Akceptacja | D+3 | D+3 | 0h | — | 100% | Klient | 1.1.1 |
| 1.1.3 | Podpisanie | D+3 | D+9 | 5h | 5.00d | 50% | Zarząd | 1.1.2 |
| 1.2 | Analiza i projektowanie | D+3 | D+17 | 170h | 3.50d | 18% | | |
| 1.2.1 | Specyfikacja | D+3 | D+9 | 60h | 5.00d | 50% | Analityk 1 | |
| 1.2.2 | Makiety | D+8 | D+14 | 38h | 4.75d | **0%** | Designer | 1.1.2 |
| 1.2.3 | Projekty graficzne | D+14 | D+17 | 24h | 3.00d | **0%** | Grafik | 1.2.2 |
| 1.2.4 | Architektura | D+7 | D+14 | 48h | 6.00d | **0%** | Analityk 1 | 1.1.2+2d |
| 1.3 | Development | D+10 | D+32 | 319h | 16.38d | **0%** | | |
| 1.3.1 | Back-end | D+10 | D+28 | 87h | 12.88d | 0% | Developer BE | |
| 1.3.2 | iOS | D+10 | D+32 | 116h | 16.38d | 0% | Developer iOS | |
| 1.3.3 | Android | D+10 | D+32 | 116h | 16.38d | 0% | Developer Android | |
| 1.4 | Testy | D+32 | D+35 | 24h | 3.00d | 0% | Tester | 1.3.2, 1.3.3 |
| 1.5 | Akceptacja rozwiązania | D+35 | D+35 | — | — | 0% | Klient | 1.4 |
| 1.6 | Wdrożenie | D+32 | D+38 | 20h | 4.50d | 0% | | |

### Załącznik 2: Zasoby projektowe

| Lp. | Rola | Alokacja | Łączne godziny |
|-----|------|----------|---------------|
| 1 | Project Manager | 100% | **0h** ⚠️ |
| 2 | Prawnik | 100% | 24h |
| 3 | Klient | 100% | 0h |
| 4 | Zarząd | 100% | 5h |
| 5 | Analityk 1 | 50% | 108h |
| 6 | Analityk 2 | 50% | 60h |
| 7 | Designer | 100% | 38h |
| 8 | Grafik | 100% | 24h |
| 9 | Developer BE | 100% | 87h |
| 10 | Developer iOS | 100% | 136h |
| 11 | Developer Android | 100% | **24h** ⚠️ (vs 116h w harmonogramie) |
| 12 | Tester | 100% | **136h** ⚠️ (vs 24h w harmonogramie) |

---

## TL;DR

Projekt znajduje się w krytycznym opóźnieniu — **10% ukończenia przy ~33% upływu czasu**. Największe zagrożenia: brak rozpoczętych makiet i architektury, brak przypisanego PM, niespójne dane zasobów. Rekomenduję natychmiastowe przypisanie PM, wewnętrzną stabilizację, spotkanie kryzysowe z klientem i rewizję harmonogramu.

---

## 1. Ocena stanu projektu i rekomendacje

### 1.1 Zidentyfikowane problemy

**Problem 1: Krytyczne opóźnienie w fazie analizy i projektowania**
- Makiety — termin minął → **0% realizacji**
- Projekty graficzne — nie mogą się rozpocząć bez makiet → **0%**
- Architektura — termin minął → **0% realizacji**
- Development zaplanowany do startu jest **zablokowany**

**Wpływ:** Bardzo wysokie ryzyko kaskadowego opóźnienia całego projektu.

**Problem 2: Brak przypisanego Project Managera**
- Plan zasobów: PM przy 100% alokacji, **0h przepracowanych**
- Przy łącznej pracochłonności 562h brak PM oznacza brak eskalacji i koordynacji

**Problem 3: Niezgodności w alokacji zasobów**

| Rola | Harmonogram (WBS) | Plan zasobów | Delta |
|------|-------------------|--------------|-------|
| Developer Android | 116h | 24h | ⚠️ -92h |
| Developer iOS | 116h | 136h | +20h |
| Tester | 24h | 136h | ⚠️ +112h |

Dane źródłowe są niespójne — wymagają korekty przed dalszym planowaniem.

**Problem 4: Niezamknięte sprawy formalne**
- Podpisanie umowy: **50%**, termin minął
- **Ryzyko:** Kontynuowanie prac bez podpisanej umowy niesie ryzyko prawne i finansowe

**Problem 5: Nierealistyczne zależności w harmonogramie**
- Development (iOS/Android) zaplanowany z zależnością na architekturę
- Architektura nie rozpoczęta, specyfikacja ukończona tylko w 50%
- Harmonogram nie odzwierciedla rzeczywistej sekwencji prac

*Zidentyfikowane problemy wskazują na jednoczesne ryzyko harmonogramowe, zasobowe i decyzyjne — wymagają podejścia systemowego, a nie punktowych korekt.*

---

### 1.2 Ocena ogólna projektu

| Obszar | Status |
|--------|--------|
| Postęp ogólny | 10% (przy ~33% oczekiwanego czasu) |
| Harmonogram | Krytyczne opóźnienie (min. 3-5 dni) |
| Budżet | Niewykorzystany; wysokie ryzyko przekroczenia |
| Zespół | Niezbalansowana alokacja zasobów |
| Ryzyko | **WYSOKIE — wymagana natychmiastowa interwencja** |

---

### 1.3 Rekomendowane działania

**Działanie 1: Przypisanie Project Managera (natychmiast)**
- Tymczasowe lub warunkowe przypisanie — bez eskalacji do klienta
- Rekomendowana alokacja: 20–30% w fazie stabilizacji
- Zakres: harmonogram, ryzyka, komunikacja, koordynacja zespołu

**Działanie 2: Wewnętrzna stabilizacja projektu**
- Weryfikacja i ujednolicenie danych (harmonogram vs zasoby)
- Identyfikacja rzeczywistej ścieżki krytycznej
- Potwierdzenie statusu umowy
- Przygotowanie co najmniej dwóch scenariuszy: pełny zakres z nowym terminem / MVP

**Działanie 3: Spotkanie kryzysowe z klientem**
- Transparentne przedstawienie stanu projektu
- Prezentacja przygotowanych scenariuszy
- Wspólna decyzja o zakresie, terminach i dalszej współpracy

**Działanie 4: Domknięcie kwestii formalno-kontraktowych**
- Podpisanie umowy lub aneksu przed kontynuacją prac

**Działanie 5: Aktualizacja harmonogramu i zależności**

Poprawiona sekwencja:
**Specyfikacja → Architektura → Makiety → Projekty graficzne → Development**

Nowe daty zakończenia:
- Pełny zakres: +8-10 dni roboczych
- MVP: +3-5 dni roboczych

**Działanie 6: Korekta alokacji zasobów**
- Zwiększenie alokacji Developer Android do poziomu zgodnego z harmonogramem
- Redukcja lub przesunięcie alokacji Testera
- Rozważenie wsparcia dodatkowego Designera

**Działanie 7: Stabilizacja trybu pracy**
- Daily stand-up (15 min)
- Checkpointy co 48h w fazach krytycznych
- Definition of Done dla kluczowych deliverables
- SLA na feedback klienta: maks. 3 dni robocze

---

### 1.4 Główne ryzyka i mitygacje

| Ryzyko | Wpływ | Mitygacja |
|--------|-------|-----------|
| Brak PM | Wysoki | Natychmiastowa alokacja |
| Brak umowy | Wysoki | Decyzja formalna + eskalacja |
| Niespójne dane zasobów | Średni | Korekta danych |
| Opóźnienia akceptacji klienta | Średni | SLA na feedback (3 dni) |

---

## 2. Analiza wymagań klienta

Klient zgłosił potrzebę mobilnej tablicy ogłoszeń z rejestracją użytkowników, możliwością dodawania ogłoszeń, powiadomieniami push, automatycznym wygasaniem ogłoszeń i płatnym przedłużaniem.

### 2.1 Wymagania funkcjonalne

1. Rejestracja i logowanie użytkownika
2. Dodawanie, edycja i przeglądanie ogłoszeń
3. Wysyłanie zapytań + powiadomienia push
4. Automatyczne wygasanie ogłoszeń
5. Płatne przedłużanie ogłoszeń

### 2.2 Wymagania niefunkcjonalne

1. iOS + Android
2. Powiadomienia push w czasie rzeczywistym
3. Bezpieczna autentykacja
4. Integracja płatności
5. SLA wydajnościowe

---

## 3. Uproszczone SOW i wycena szacunkowa

### 3.1 Zakres i pracochłonność

| Faza | Godziny |
|------|---------|
| Discovery & Design | 108h |
| Backend Development | 192h |
| Mobile iOS | 140h |
| Mobile Android | 140h |
| QA & Testing | 76h |
| Deployment & Launch | 48h |
| Project Management | 84h |
| **SUMA** | **788h** |

*SOW obejmuje pełny zakres — szerszy niż pierwotny harmonogram (562h) ze względu na alokację PM, bufory i skorygowany plan zasobów.*

### 3.2 Timeline
- Całkowity czas realizacji: **12-14 tygodni**
- Prace prowadzone iteracyjnie (Agile/Scrum)

### 3.3 Koszt szacunkowy
**Rekomendacja:** 200 000 – 280 000 PLN netto (zespół Mid/Senior mix)

*Szacunki oparte na dekompozycji zakresu, porównaniu z podobnymi realizacjami i buforach ryzyk integracyjnych. Wycena do doprecyzowania po warsztatach z klientem.*

---

*Dokument zanonimizowany — nazwy firmy, projektu i niektóre dane liczbowe zostały zmienione w celu ochrony poufności. Zmiany nie wpływają na wnioski analityczne ani rekomendacje. Cała analiza, rekomendacje i wyceny są oryginalną pracą autorki.*

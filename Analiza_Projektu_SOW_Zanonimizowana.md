# Analiza projektu i wycena SOW: Mobilna tablica ogłoszeń
**Autor:** Nastka Dąbrowska
**Kontekst:** Analiza dla klienta zewnętrznego software house'u — ocena stanu projektu, analiza wymagań i szacowanie pracochłonności.

---

## TL;DR

Projekt znajduje się w krytycznym opóźnieniu — **10% ukończenia przy ~33% upływu czasu**. Największe zagrożenia: brak rozpoczętych makiet i architektury, brak przypisanego PM. Rekomenduję natychmiastowe przypisanie PM, wewnętrzną stabilizację projektu, spotkanie kryzysowe z klientem i rewizję harmonogramu.

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
- Deadline: natychmiast

**Działanie 2: Wewnętrzna stabilizacja projektu**
- Weryfikacja i ujednolicenie danych (harmonogram vs zasoby)
- Identyfikacja rzeczywistej ścieżki krytycznej
- Potwierdzenie statusu umowy
- Przygotowanie co najmniej dwóch scenariuszy: pełny zakres z nowym terminem / zakres ograniczony (MVP)
- Deadline: 1-2 dni

**Działanie 3: Spotkanie kryzysowe z klientem**
- Transparentne przedstawienie stanu projektu
- Prezentacja przygotowanych scenariuszy
- Wspólna decyzja o zakresie, terminach i dalszej współpracy
- Deadline: 2 dni od stabilizacji wewnętrznej

**Działanie 4: Domknięcie kwestii formalno-kontraktowych**
- Potwierdzenie zakresu i warunków dalszej współpracy
- Podpisanie umowy lub aneksu
- Deadline: 3 dni

**Działanie 5: Aktualizacja harmonogramu i zależności**

Poprawiona sekwencja zależności:
**Specyfikacja → Architektura → Makiety → Projekty graficzne → Development**

Nowe daty zakończenia:
- Pełny zakres: +8-10 dni roboczych od pierwotnego terminu
- MVP: +3-5 dni roboczych

**Działanie 6: Korekta alokacji zasobów**
- Zwiększenie alokacji Developer Android do poziomu zgodnego z harmonogramem
- Redukcja lub przesunięcie alokacji Testera
- Rozważenie wsparcia dodatkowego Designera w fazie projektowej

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

### 2.1 Wymagania funkcjonalne

1. Rejestracja i logowanie użytkownika
2. Dodawanie, edycja i przeglądanie ogłoszeń
3. Wysyłanie zapytań i powiadomienia push
4. Automatyczne wygasanie ogłoszeń
5. Płatne przedłużanie ogłoszeń

### 2.2 Wymagania niefunkcjonalne

1. iOS + Android
2. Powiadomienia push w czasie rzeczywistym
3. Bezpieczna autentykacja
4. Integracja płatności
5. SLA wydajnościowe (np. czas odpowiedzi kluczowych widoków)

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

*SOW obejmuje pełny zakres projektu — szerszy niż pierwotny harmonogram (562h) ze względu na alokację PM, bufory i skorygowany plan zasobów.*

### 3.2 Timeline
- Całkowity czas realizacji: **12-14 tygodni**
- Prace prowadzone iteracyjnie (Agile/Scrum)

### 3.3 Koszt szacunkowy
**Rekomendacja:** 200 000 – 280 000 PLN netto (zespół Mid/Senior mix)

*Szacunki pracochłonności oparte na dekompozycji zakresu prac na poziomie zadań, porównaniu z podobnymi realizacjami oraz buforach wynikających z ryzyk integracyjnych. Wycena ma charakter szacunkowy — do doprecyzowania po warsztatach z klientem.*

---

*Dokument zanonimizowany. Nazwy firmy i projektu zostały usunięte. Cała analiza, rekomendacje i wyceny są oryginalną pracą autorki.*

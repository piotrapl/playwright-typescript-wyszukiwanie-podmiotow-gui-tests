# Testy automatyczne REGON – Playwright (TypeScript)

## 📌 Opis projektu
Projekt jest zestawem **testów automatycznych UI (E2E)** napisanych w **Playwright + TypeScript**, przygotowanym jako część **portfolio QA Automation**.

Testy weryfikują funkcjonalność wyszukiwania firm po numerze **REGON** na oficjalnej stronie rządowej:
https://wyszukiwarkaregon.stat.gov.pl

---

## 🎯 Testowana funkcjonalność
- Wyszukiwanie firmy po numerze **REGON**
- Walidacja błędnych numerów REGON
- Wyświetlanie danych firmy dla poprawnych REGONów

---

## 🧪 Scenariusze testowe
### Przypadki negatywne
- REGON o nieprawidłowej długości
- REGON z błędną cyfrą kontrolną
- REGON zawierający znaki nienumeryczne

### Przypadki pozytywne
- Poprawny REGON 9-cyfrowy → firma znaleziona
- Poprawny REGON 14-cyfrowy → firma znaleziona

---

## 🛠️ Technologie i narzędzia
- **Playwright**
- **TypeScript**
- **Playwright Test Runner**
- **Raport HTML**
- **GitHub Actions (gotowe pod CI)**

---

## 🧩 Zastosowane dobre praktyki automatyzacji
- ✅ Własne **fixtures Playwright**
- ✅ Testy data-driven
- ✅ Odporne selektory (ARIA, regex)
- ✅ Assercje odporne na zmiany treści UI
- ✅ Zrzuty ekranu dla **każdego testu** (PASS i FAIL)
- ✅ Screenshoty dołączone do raportu HTML
- ✅ Czytelna i łatwa w utrzymaniu struktura testów

---

## ▶️ Uruchamianie testów lokalnie
```bash
npm install
npx playwright test
npx playwright show-report

## Możliwe usprawnienia, optymalizacje:

- 🔹 Dodanie **testów API**, niezależnych od warstwy UI
- 🔹 Przyspieszenie testów poprzez **mockowanie odpowiedzi sieciowych**
- 🔹 Wprowadzenie **testów regresji wizualnej**
- 🔹 Udoskonalenie selektorów przy użyciu **test ID** (jeśli dostępne)
- 🔹 Oznaczanie lub izolacja **niestabilnych testów**
- 🔹 Lepsze logowanie i obsługa błędów testowych
- 🔹 Kategoryzacja testów przy użyciu **tagów Playwright**

## Co można dodać do tego projektu, w jaki sposób go rozszerzyć ?

- **Pipeline CI/CD** z GitHub Actions (równoległe uruchamianie testów, artefakty)
- **Analizę wyników testów** i dashboardy
- **Testy wieloprzeglądarkowe** (Chromium, Firefox, WebKit)
- **Testy w widokach mobilnych**
- Testy **wielojęzyczności (i18n)**
- Zewnętrzne źródła danych testowych (JSON / CSV)
- Testy bezpieczeństwa i dostępności (podstawowa walidacja a11y)
- Podejście hybrydowe: testy UI + API + komponentowe
- Rozszerzone raportowanie (metadane, środowisko, konfiguracja)
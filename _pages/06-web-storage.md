---
title: Web Storage
layout: post
---

### Ogólne informacje

- Składa się z `sessionStorage` i `localStorage`.
- Pozwala na przechowywanie danych tylko po stronie klienta.
- Można w nim przechować więcej danych, ok. 1000 razy więcej niż w ciastkach.

### Rodzaje Web Storage

1. **sessionStorage**
    - Oddzielna przestrzeń na dane dla każdego źródła dokumentów*.
    - Dostępna podczas jednej sesji przeglądarki (tak długo jak przeglądarka jest otwarta, wliczając przeładowania strony i odtwarzanie stron po zamknięciu przeglądarki - nie jest to zawsze gwarantowane, moze zalezeć od ustawień przeglądarki).
    - Każda zakładka lub okno ma swoją własną przestrzeń na dane, nawet jeśli pochodzą z tej samej domeny


2. **localStorage**
    - Robi to samo, co `sessionStorage`.
    - Dane przechowywane są na stałe nawet po zamknięciu przeglądarki (bez limitu czasowego).
    - Dane są dostępne dla wszystkich okien i zakładek z tej samej domeny

\* Źródło dokumentów definiowane jest przez protokół, domenę i port (np: `https://www.mojadomena.pl:6666`).

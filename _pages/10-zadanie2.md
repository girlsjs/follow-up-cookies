---
title: 10. Funkcje
layout: post
---

Celem naszego drugiego zadania będzie odczytanie po naciśnięciu przycisku Restore kolorów zapisanych w `localStorage` i `sessionStorage` oraz ustawienie ich jako aktualnych na stronie.

**Znowu potrzebny jest plan!**

### 👉 Plan działania
- Odczytaj wartość zapisaną w `localStorage`
- Ustaw ją jako aktualny kolor tła
- Odczytaj wartość zapisaną w `sessionStorage`
- Ustaw ją jako aktualny kolor tekstu


Spróbujmy napisać funkcję `restoreColors`, która realizuje drugie zadanie!  

Czy możemy wykorzystać istniejący już kod? 🤔

#### Gotowe?

Wyszło nam pewnie coś takiego:
```javascript
function restoreColors() {
  const bgColor = localStorage.getItem('backgroundColor');
  const fgColor = sessionStorage.getItem('color');

  setBackground(bgColor);
  setForeground(fgColor);
}
```

Pozostało nam tylko połączenie funkcji `restoreColors()` ze zdarzeniem kliknięcia na przycisk `Restore`.

```javascript
document
  .querySelector('#restore')
  .addEventListener('click', restoreColors);
  ```

### 👉 Testowanie

Sprawdźmy w praktyce jak działa Web Storage

#### Test 1
1. Ustaw nowe kolory tła i tekstu.
2. Zapisz je w Web Storage naciskając Save.
3. Otwórz w nowej zakładce drugą kopię strony `webstorage.html`.
4. Odtwórz kolory w otwartym przed chwilą dokumencie naciskając Restore.
5. Co udało się zaobserwować?

#### Test 2
1. Ustaw nowe kolory tła i tekstu w drugiej zakładce.
2. Zapisz je w Web Storage naciskając Save.
3. Otwórz pierwszą zakładkę ze stroną `webstorage.html`.
4. Naciśnij przycisk Restore.
5. Co udało się zaobserwować?

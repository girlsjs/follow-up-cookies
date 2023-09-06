---
title: "Zadanie 1"
layout: post
---

Pobierz paczkę z kodem źródłowym: [LINK - cookies.zip](https://girlsjs.github.io/kurs/follow-ups/cookies/cookies.zip)

Po wypakowaniu znajdziesz w głównym folderze kilka plików.
Nas w tej chwili interesuje `webstorage.html`.


### 👉 Uruchom swój własny serwer
1. otwórz Visual Studio Code
2. otwórz folder z pobranym kodem źródłowym
3. upewnij się, że masz dodaną i aktywowaną wtyczkę do VSC - Live Server
4. wejdź w plik `webstorage.html` > klinij prawym przyciskiem myszki i wybierz "Otwórz za pomocą Live Server"

### 👉 Na razie bez zaglądania do kodu
- Otwarta strona `webstorage.html` zawiera prosty formularz, za pomocą którego możemy zmieniać kolor tła i tekstu. Sprawdźmy przez chwilę, jak to działa. 

- Są tu również dwa przyciski, które nic nie robią (na razie). Otwórzmy plik `webstorage.html` w swoim ulubionym edytorze i popatrzmy przez chwilę na kod.

### 👉 Pierwsze zadanie
Celem naszego pierwszego zadania będzie zapisanie po naciśnięciu przycisku Save aktualnie ustawionych kolorów w localStorage i sessionStorage

  - Kolor tła zapiszmy w `localStorage`.
  - Kolor tekstu zapiszmy w `sessionStorage`.

### 👉 Jak się do tego zabrać?
1. Pobierz aktualny kolor tła.
2. Zapisz wartość w `localStorage`.
3. Pobierz aktualny kolor tekstu.
4. Zapisz wartość w `sessionStorage`.

To nie było trudne, tylko skąd wziąć aktualne wartości kolorów?  

Spróbujmy napisać funkcję w js `saveColors()`, która realizuje pierwsze zadanie!
 
Czy możemy wykorzystać istniejący już kod? 🤔

#### Gotowe?  

Wyszło nam pewnie coś takiego:

```javascript
function saveColors() {
  const currentBgColor = document.body.style.backgroundColor;
  const currentColor = document.body.style.color;
  
  localStorage.setItem("backgroundColor", currentBgColor.toString());
  sessionStorage.setItem("color", currentColor.toString());
}
```

Teraz zastanówmy się co zrobić, żeby kliknięcie w przycisk uruchomiło naszą funkcję?

```javascript
document
  .querySelector('#save')
  .addEventListener('click', saveColors);
```

No dobrze, ale jak właściwie sprawdzić, czy coś się wydarzyło?

Otwórzmy narzędzia programisty i zajrzyjmy do zakładki Aplikacja


![](/cookies/assets/localstorage.png)
*localStorage*


![](/cookies/assets/sessionstorage.png)
*sessionStorage*
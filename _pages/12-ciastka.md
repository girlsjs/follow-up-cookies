---
title: Pora na ciastka 🍪
layout: post
---

### Zapisujemy różne informacje w przeglądarce

W myśl obowiązujących przepisów powinno się poprosić o zgodę, co niezwłocznie uczynimy. W tym celu wykorzystamy nieużywany jeszcze element `aside` na stronie `webstorage.html`. 

Zawiera on notyfikację o ciasteczku oraz przycisk do jej zamknięcia. Jedyny problem jest taki, że ta notyfikacja się **nie wyświetla** na stronie.

#### 👉  Sprawdźmy dlaczego

Pomyślmy nad scenariuszem, który powinien być realizowany podczas ładowania strony. Jakie musimy uwzględnić wymagania?

- Pokaż notyfikację o ciasteczkach, jeśli użytkownik jest u nas pierwszy raz
- Schowaj notyfikację, gdy użytkownik wyrazi zgodę na ciasteczka
- Nie nękaj go więcej notyfikacjami (powiedzmy przez nadchodzący rok)

#### 👉  Scenariusz, który chcemy zrealizować

1. Sprawdź, czy użytkownik ma zapisane nasze **magiczne ciasteczko**.
2. Jeśli nie, natychmiast pokaż notyfikację o ciasteczkach.
3. Gdy wyrazi zgodę, ukryj notyfikację i zapisz nasze magiczne ciasteczko z rocznym terminem przydatności do spożycia.

#### 👉 Krok 1. Sprawdź ciasteczko

Napiszmy funkcję `isCookieSet()`, która przyjmie nazwę ciasteczka jako jedyny parametr i zwróci wartość logiczną `true` / `false` mówiącą o tym, czy ciasteczko o podanej nazwie jest ustawione.

<details>
  <summary>💡 Kliknij tutaj, aby zobaczyć rozwiązanie</summary>

  **Rozwiązanie: **

  ```js
  function isCookieSet(name) {
    const cookies = document.cookie.split('; ');
    for (let i = 0; i < cookies.length; i += 1) {
      if (cookies[i].startsWith(name + '=')) {
        return true;
      }
    }
    return false;
  }
  ```
</details>

#### 👉 Krok 2. Pokaż notyfikację o ciasteczkach

Skorzystamy tu z `element.classList` i `classList.remove()`

Napiszmy funkcję `showCookieNotice()`, która pokaże element `aside`
oraz połączmy jej działanie z funkcją z kroku pierwszego.

```javascript

function showCookieNotice() {
  document.querySelector('#cookie-notice').classList.remove('hide');
}

if ( !isCookieSet('accept-cookies') ) {
  showCookieNotice();
}
```

#### 👉 Krok 3. Ukryj notyfikację i zapisz ciasteczko

Ten krok podzielimy na dwie niezależne części.

* Po pierwsze potrzebujemy funkcji `hideCookieNotice()` (ukryj) działającej odwrotnie do funkcji z kroku drugiego. Skorzystamy tu z metody `classList.add()`.

```javascript
function hideCookieNotice() {
  document.querySelector('#cookie-notice').classList.add('hide');
}
```

* Po drugie potrzebujemy fukncji, która zapisze ciasteczko w przeglądarce.

Nasza funkcja `setCookie()` powinna przyjmować nazwę ciasteczka, jego wartość i opcjonalnie czas przydatności do "spożycia" ;)

Oto jedno z możliwych rozwiązań:

```javascript

function setCookie(name, value, time) {
  let cookie = name + '=' + value;
  if (time) {
    cookie += '; max-age=' + time;
  }
  document.cookie = cookie;
}
```

#### 👉 Pozostaje nam tylko połączenie wszystkich elementów

```javascript
function acceptCookies() {
  hideCookieNotice();
  setCookie('accept-cookies', true, 60*60*24*365);
}

document
  .querySelector('#cookie-notice-button')
  .addEventListener('click', acceptCookies);
```


👉 **Czas próby!**

Zapisujemy naszą stronę, odświeżamy i patrzymy co się dzieje

Wszystko gra?

![](/cookies/assets/we-dit-it.gif)
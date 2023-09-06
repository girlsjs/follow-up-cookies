---
title: "> SessionStorage"
layout: post
---

## Jak działa Session Storage?

`sessionStorage` to inny mechanizm dostępny w przeglądarkach internetowych, który różni się od `localStorage` tym, że przechowuje dane tylko na czas jednej sesji przeglądarki.

Podobnie jak w przypadku `localStorage`, można zapisywać i odczytywać dane w `sessionStorage` za pomocą JavaScript.


### Mechanizm działania

Działa to w ten sposób:

- Kiedy użytkownik otwiera nowe okno lub kartę i przechodzi na stronę, rozpoczyna się nowa sesja.
- Dane zapisane w `sessionStorage` są dostępne tylko podczas tej konkretnej sesji.
- Jeśli użytkownik zamknie okno lub kartę, dane w `sessionStorage` są automatycznie usuwane.

### Zastosowanie

- `sessionStorage` jest użyteczny do przechowywania tymczasowych danych, takich jak stan aplikacji czy preferencje użytkownika.
- Po zakończeniu sesji, dane są usuwane, co pomaga w utrzymaniu prywatności i ogranicza ryzyko przekroczenia limitu pamięci.

### Podstawowe użycie session storage

1. **Zapisywanie danych do session storage**
    ```javascript
    sessionStorage.setItem('nazwa', 'wartość');
    ```

2. **Odczyt z session storage i zapisanie do zmiennej**
    ```javascript
    const data = sessionStorage.getItem('nazwa');
    ```

3. **Usuwanie danych z session storage**
    ```javascript
    sessionStorage.removeItem('nazwa');
    ```

4. **Usuwanie całej zawartości session storage**
    ```javascript
    sessionStorage.clear();
    ```
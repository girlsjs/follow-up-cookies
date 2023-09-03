---
title: "> LocalStorage"
layout: post
---


## 👉 Jak działa localStorage?

`localStorage` to mechanizm dostępny w przeglądarkach internetowych umożliwiający przechowywanie danych na stałe na poziomie przeglądarki. Pozwala to na zapisanie informacji, takich jak ciasteczka, na komputerze użytkownika nawet po zamknięciu przeglądarki. 

Dane `zapisane`` w localStorage są dostępne na poziomie domeny, co oznacza, że są udostępniane między stronami tej samej witryny. To idealne rozwiązanie do przechowywania niewielkich ilości danych, takich jak preferencje użytkownika czy ustawienia aplikacji, bez potrzeby wysyłania ich na serwer.

### Charakterystyka

- **Przechowywanie danych**: Dane są przechowywane na stałe, nawet po zamknięciu przeglądarki.
- **Dostępność**: Dane są dostępne na poziomie domeny, co oznacza, że są udostępniane między stronami tej samej witryny.

### Podstawowe użycie localStorage

1. **Zapisywanie danych**
    ```javascript
    localStorage.setItem('nazwa', 'wartość');
    ```

2. **Odczyt danych**
    ```javascript
    const data = localStorage.getItem('nazwa');
    ```

3. **Usuwanie danych**
    ```javascript
    localStorage.removeItem('nazwa');
    ```

4. **Usuwanie całej zawartości**
    ```javascript
    localStorage.clear();
    ```

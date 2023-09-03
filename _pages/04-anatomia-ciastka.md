---
title: Anatomia ciastka
layout: post
---

Juz wiesz, że pliki cookies to małe fragmenty danych, które strony internetowe zapisują na twoim komputerze. 

Służą one do różnych celów, takich jak zapamiętywanie twoich preferencji czy śledzenie twojej aktywności online, pokazywaniu lepiej dopasowanych reklam. 

Przyjrzyjmy się jednak dokładniej z czego skłda się ciastko!

### Elementy ciastka

1. **Nazwa**: Unikalna nazwa ciasteczka, za pomocą której można je identyfikować.
2. **Wartość**: Dane przechowywane w ciasteczku, na przykład preferencje użytkownika.
3. **Domena**: Domena, dla której ciasteczko jest dostępne.
4. **Ścieżka**: Ścieżka na serwerze, dla której ciasteczko jest dostępne.
5. **Wygaśnięcie (Expires)**: Określa, kiedy ciasteczko zostanie usunięte.
6. **Zabezpieczenia**: Atrybuty bezpieczeństwa, takie jak:
    - **Secure**: Ciasteczko wysyłane tylko przez protokół HTTPS.
    - **HttpOnly**: Ciasteczko niedostępne dla skryptów.



Spośród tych atrybutów tym razem najbardziej interesuje nas nie liczba kalorii, ale data ważności 😜

## Jak można zapisać dane w przeglądarce?

### Metody przechowywania danych

1. **HTTP Cookies**: 
    - Dostępne z poziomu JavaScript.
    - Mają ograniczoną wielkość.
    - Są wysyłane z każdym żądaniem HTTP.

2. **Web Storage**: 
    - Składa się z `sessionStorage` i `localStorage`.
    - Pozwala na przechowywanie danych tylko po stronie klienta.

3. **IndexedDB**: 
    - Zaawansowana baza danych w przeglądarce.
    - Pozwala na przechowywanie większych ilości danych w obiektach.

![](/cookies/assets/gif_cookies.gif)
*Przypomnienie: narzędzia programisty w Chrome włączamy przez F12 (Command+Option+I na macOS)*


![](/cookies/assets/cookies-screen.png)
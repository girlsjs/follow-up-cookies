---
title: HTTP cookies
layout: post
---

Ciasteczka w Twojej przeglądarce

### Charakterystyka

- Mają ograniczoną wielkość.
- Są wysyłane z każdym żądaniem HTTP.

### Manipulacja ciasteczkami za pomocą `document.cookie`

👉  **Odczytywanie wszystkich ciasteczek**

```javascript
    const allCookies = document.cookie;
    // np. => 'nazwa1=wartość1; nazwa2=wartość2; nazwa3=wartość3'
```

 👉  **Zapisywanie ciasteczka**

```javascript
    document.cookie = 'nazwa=wartosc; max-age=3600';
```

> ##### UWAGA
>
>`document.cookie` działa bardziej jak wpłatomat, niż normalna zmienna. Zapisanie ciasteczka nie nadpisuje innych ciasteczek.
{: .block-warning }


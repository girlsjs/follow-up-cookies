---
title: "- Zadanie 3"
layout: post
---

Poniżej ramki z formularzem znajduje się odnośnik, zróbmy z niego użytek!

W nowej zakładce powinien się otworzyć dokument `webstoragemonitor.html`.

Umieśćmy oba dokumenty obok siebie, tak aby były jednocześnie widoczne.

Czas na magię - zmieńmy kolor tła i zapiszmy nową wartość w WebStorage.

### Analiza dokumentu `webstoragemonitor.html`

Otwórzmy dokument `webstoragemonitor.html` w naszym ulubionym edytorze i zobaczmy, co tam się dzieje.

- Czy wszystko jasne? Nie wygląda to aż tak magicznie 😊
- Spróbujmy zrobić jakiś użytek z tego, co widzimy

### Zadanie

- Sprawmy, aby strona `webstoragemonitor.html` zmieniła kolor tła za każdym razem, gdy zmieniamy go i zapisujemy na stronie `webstorage.html`.

- Otwórzmy plik `webstoragemonitor.html` i napiszmy funkcję `setStyle`, która ustawi kolor tła dokumentu za każdym razem, gdy pojawi się zdarzenie związane z Web Storage.

```javascript

// Funkcja setStyle, która zmienia kolor tła
function setStyle(ev) {
  document.body.style[ev.key] = ev.newValue;
}

window.addEventListener('storage', setStyle);
```


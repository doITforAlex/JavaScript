---
layout: step
number: 3
title: Zmienne
permalink: step3/
---

Wiesz już, czym są dane, operacje arytmetyczne i wyrażenia.

A co w sytuacji, kiedy jeszcze nie znamy danej wartości, a i tak chcemy jej użyć? Albo jeżeli będzie się ona zmieniać? W takiej sytuacji przydadzą się nam zmienne.

**Zmienne** to nazwane "pudełka", w których przechowywane sa nasze dane.

Żeby stworzyć nową zmienną musisz zadeklarować jej nazwę z użyciem słowa kluczowego `let` (dla zmiennych, które będziemy modyfikować) lub `const` (dla zmiennych, które nie będą się zmieniać, ciągle będą miały jedną i tę samą wartość):

```javacript
let wiadomosc;
```

Stworzyliśmy w ten sposób nową zmienną o nazwie `wiadomosc`.

W starszym kodzie możesz zobaczyć też, że zmienne tworzono za pomocą innego słowa kluczowego, `var`, na przykład:

```javacript
var wiadomosc;
```

Jest to jednak przestarzały zapis, a obecnie używa się słów `let` i `const` - tak więc właśnie z nich będziemy dzisiaj korzystać.

A jakie są zasady tworzenia nazw zmiennych?

- mogą zawierać litery, cyfry, podkreślniki (`_`) i znaki dolara,
- muszą zaczynać się od litery,
- wielkość liter ma znaczenie (przykładowo `wiadomosc` i `Wiadomosc` to dwie różne zmienne),
- nie mogą być słowami zastrzeżonymi (w javascript takimi słowami są m.in. `let` czy `const`),
- nazwy zmiennych powinny być po angielsku (chociaż dla lepszej czytelności w przykładach będziemy dzisiaj używać polskich nazw, ale bez polskich znaków),
- jeżeli nazwa zmiennej składa się z kilku słów, zapisujemy ją w formie **camelCase** (tzw. notacja wielbłądzia, taki zapis to na przykład _`nazwaZmiennej`_) albo kebab-case (nazwa mówi sama za siebie, taki zapis to na przykład _`nazwa-zmiennej`_) - zwykle spotkasz się jednak z zapisem camelCase.

Po stworzeniu zmiennej możesz przypisać do niej jakąś wartość za pomocą **operatora przypisania**, czyli znaku `=`.

```javascript
wiadomosc = "Witaj!";
```

Zwróć uwagę, że stworzenie (zadeklarowanie) zmiennej i przypisanie do niej wartości możesz też zrobić razem, jednym wyrażeniem:

```javascript
let wiadomosc = "Witaj!";
```

Przypisywanie do zmiennej wartości podczas jej tworzenia nazywane jest także **inicjalizacją**.

<!-- Zmienna bez przypisanej wartości zawiera specjalną wartość - `undefined`. `undefined` to nie string z tym słowem, tylko zupełnie inny typ wartości -->

Zmienna to takie opisane pudełko, w którym przechowujesz jakieś dane i później możesz się do nich odwoływać używając nazwy tego pudełka.

A więc, przykładowo, możesz zmodyfikować naszą funkcję `zrobCos()` w następujący sposób:

```javascript
function zrobCos() {
  let wiadomosc = "Naciśnięto przycisk!";
  document.getElementById("okno").innerText = wiadomosc;
}
```

Ale to taki typowo książkowy przykład, który nie obrazuje za dobrze, _po co_ używamy zmiennych.

Wyjaśnijmy to na lepszym przykładzie.

Zmodyfikujemy naszą stronę w ten sposób, że będzie miała teraz trzy przyciski - `Przyjdź`, `Odejdź` i `Powiedz coś`.
Po naciśnięciu na przycisk `Powiedz coś`, wyświetlona zostanie wiadomość, którą przypiszemy do zmiennej.
Naciśnięcie na przycisk `Przyjdź` i `Odejdź` spowoduje zmianę treści wiadomości.

Napiszmy w takim razie naszą kolejną stronę:

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8" />
    <title>Warsztaty z JSa!</title>
  </head>
  <body>
    <button id="przyciskPrzyjdz">Przyjdź</button>
    <button id="przyciskOdejdz">Odejdź</button>
    <button id="przyciskPowiedzCos">Powiedz coś</button>
    <pre id="okno"></pre>
  </body>
  <script>
    let wiadomosc = "Nie wiem, gdzie jesteś!";

    function przyjdz() {
      wiadomosc = "Witaj!";
    }

    function odejdz() {
      wiadomosc = "Szerokiej drogi!";
    }

    function powiedzCos() {
      document.getElementById("okno").innerText = wiadomosc;
    }

    document.getElementById("przyciskPowiedzCos").onclick = powiedzCos;
    document.getElementById("przyciskPrzyjdz").onclick = przyjdz;
    document.getElementById("przyciskOdejdz").onclick = odejdz;
  </script>
</html>
```

Jak widzisz, w naszym kodzie używamy zmiennej `wiadomosc`, która wyświetla się po kliknięciu na przycisk `Powiedz coś`. Z kolei kliknięcie na przycisk `Przyjdź` lub `Odejdź` spowoduje, że do naszej zmiennej `wiadomosc` przypisany zostanie inny tekst.

Zanim pójdziemy dalej, spróbuj dodać na stronie kolejny przycisk, `Zostań`, po kliknięciu na który wiadomość zostanie zmieniona na `Rozgość się`.

---
layout: step
number: 0
title: O programowaniu
permalink: step0/
---

Zanim zaczniemy, powiedzmy sobie krótko, czym tak właściwie jest programowanie.

Domyślamy się, że znasz już trochę HTMLa i CSSa, ale to nie jest programowanie w takim sensie, w jakim mówimy o nim tutaj. Dlaczego? HTML i CSS dotyczą wyglądu i zawartości dokumentu - które oczywiście również są ważne, ale po prostu to coś innego niż typowe programowanie.

A więc _czym tak właściwie jest programowanie_?

## Lista zadań dla komputera

Programowanie możemy porównać do tworzenia listy zadań dla komputera.

Jak zapewne wiesz, komputer sam w sobie nie podejmuje żadnych działań - najpierw musisz mu dać instrukcje, które ma wypełnić.

Problemem jest tylko to, że komputery nie są zbyt inteligentne, nie potrafią samodzielnie myśleć czy wydawać osądów. Nie mogą tak po prostu "zrozumieć" o co Ci chodzi. Robią dokładnie to, co im każesz – czasem lepiej, a czasem gorzej. A kiedy podejmują decyzję, mogą dokonać tylko tych wyborów, co do których wcześniej przekazałeś lub przekazałaś im jakieś instrukcje.

Komputery nie potrafią wypełniać skomplikowanych instrukcji, czyli Twoja lista zadań powinna być jak najprostsza.

A więc - co możesz kazać zrobić komputerowi?

1. Przechowywać dane – w programowaniu zapisujemy je jako **zmienne**.
2. Wykonać obliczenia matematyczne na danych – to **operacje arytmetyczne**.
3. Porównać dane żeby podjąć decyzję, co zrobić dalej – to **instrukcje warunkowe**.
4. Powtórzyć jakieś działania określoną liczbę razy – to **pętle**.
5. Połączyć razem kilka instrukcji, dzięki czemu mogą być używane jako jedna większa instrukcja - to **funkcje**.

I to tak właściwie wszystko.

Ale co wyświetlaniem różnych rzeczy na stronie? Albo odczytywaniem i zapisywaniem plików? Pozyskiwaniem danych wprowadzonych przez użytkowanika? Wysyłaniem zapytania do serwera? Jak zrobić te wszystkie rzeczy?

Do tego wykorzystujemy **funkcje**, które są już wbudowane w język programowania. Większość języków posiada wiele gotowych funkcji, które wykonują najróżniejsze działania.

## Programowanie w przeglądarce internetowej

Przeglądarki internetowe zapewniają nam pewną "standardową bibliotekę" funkcji, które możemy wykorzystać do robienia różnych ciekawych rzeczy w JavaScripcie.

Takich funkcji jest naprawdę wiele, ale dzisiaj będziemy zajmować się tymi, które nazywamy **Document Object Model API** - albo w skrócie po prostu **DOM API**. Skrót **API** oznacza interfejs programistyczny aplikacji, czyli to po prostu takie mądre określenie na funkcje, które pozwalają Ci na działanie z programem.
Z kolei **DOM** to odwzorowanie strony (dokumentu), które widzimy z poziomu JavaScriptu.

DOM API posiada pewne funkcje, których możemy używać do odczytywania i zmieniania zawartości strony. Właśnie za ich pomocą będziemy wyświetlać informacje użytkownikom i pozyskiwać je od nich.

Jeżeli chcesz, możesz przeczytać więcej o tym, co robią przeglądarki, tutaj: [Web API](https://developer.mozilla.org/en-US/docs/Web/Reference/API)

A teraz, skoro już mamy za sobą ten krótki wstęp, zabierajmy się za programowanie!

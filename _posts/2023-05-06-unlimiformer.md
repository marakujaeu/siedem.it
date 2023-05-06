---
layout: post
title: "Unlimiformer: Jak podsumować dowolnie długi tekst za pomocą Unlimiformera?"
categories: [Wiadomości]
tags: [Github, duże modele językowe]
author: adam
---

Podsumowywanie tekstu to zadanie, które polega na stworzeniu krótkiego i zwięzłego streszczenia dłuższego tekstu. Jest to przydatne narzędzie dla osób, które chcą szybko zapoznać się z treścią artykułu, książki lub innego dokumentu. Jednak większość istniejących metod podsumowywania tekstu ma ograniczenie: nie mogą one obsłużyć bardzo długich tekstów wejściowych, ponieważ wymagają one uwzględnienia każdego słowa w tekście. Co zrobić, jeśli chcemy podsumować całą książkę lub wiele dokumentów na raz?

![image](https://user-images.githubusercontent.com/42593540/236538293-1d5fdfe3-3e34-4979-9611-a9c9f56e3a00.png)

Odpowiedzią na to pytanie jest Unlimiformer: nowe podejście do podsumowywania tekstu, które może obsłużyć nieograniczoną długość wejścia. Unlimiformer jest oparty na transformatorach: modelach uczenia maszynowego, które potrafią zrozumieć i wygenerować tekst. Transformatory składają się z dwóch części: kodera i dekodera. Koder analizuje tekst wejściowy i tworzy reprezentację jego znaczenia. Dekoder używa tej reprezentacji, aby stworzyć tekst wyjściowy, czyli podsumowanie.

Unlimiformer różni się od innych transformatorów tym, że nie musi zwracać uwagi na każde słowo w tekście wejściowym. Zamiast tego używa on specjalnego indeksu, który przechowuje informacje o wszystkich słowach w tekście i potrafi szybko znaleźć te najważniejsze dla danego zadania. Dzięki temu Unlimiformer może indeksować bardzo długie teksty wejściowe i podsumowywać je bez żadnego obcinania.

Unlimiformer został przetestowany na kilku zestawach danych do podsumowywania długich dokumentów i wielu dokumentów. Wyniki pokazują, że Unlimiformer może podsumować nawet 350 tysięcy słów z zestawu danych BookSum, który zawiera streszczenia książek¹. Unlimiformer poprawia również wyniki innych modeli transformatorowych, takich jak BART i Longformer, rozszerzając je do nieograniczonych wejść bez dodawania nowych parametrów lub zmiany kodu.

Unlimiformer jest [dostępny publicznie wraz z kodem i modelami pod tym adresem URL](https://arxiv.org/abs/2305.01625). Jest to przełomowe narzędzie dla osób, które chcą podsumować dowolnie długi tekst za pomocą transformatorów.
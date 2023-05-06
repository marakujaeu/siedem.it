---
layout: post
title: "Googler: Nie mamy przewagi, ale OpenAI też nie"
categories: [Wiadomości]
tags: [Google, OpenAI, duże modele językowe]
author: adam
---1
  
Wyciekł wewnętrzny dokument Googlera, który Twierdzi, że Open Source AI wyprzedzi Google i OpenAI.
  
Poniższy tekst jest bardzo świeżym wyciekiem dokumentu, który został udostępniony przez anonimową osobę na publicznym serwerze Discord, która wyraziła zgodę na jego ponowne opublikowanie. Pochodzi od badacza w Google. Jego autentyczność jest zweryfikowana. Jedynymi modyfikacjami są formatowanie i usunięcie linków do wewnętrznych stron internetowych oraz tłumaczenie na język polski. Dokument jest tylko opinią pracownika Google, a nie całej firmy. Nie utożsamiamy się z tym, co jest napisane poniżej, ani inni badacze, którzy zostali o to zapytani. Sam dokument natomiast porusza bardzo interesujące kwestie, dlatego pojawia się on na łamach siedem.it.
  
## Nie mamy przewagi, ale OpenAI też nie
  
Dużo patrzymy za siebie na OpenAI. Kto przekroczy następny kamień milowy? Jaki będzie następny ruch?
  
Ale niewygodną prawdą jest, że nie jesteśmy w pozycji, aby wygrać tę wyścig zbrojeń, a OpenAI też nie. Podczas gdy my się kłócimy, trzecia frakcja cicho nam zjada obiad.
Mówię oczywiście o open source. Po prostu nas wyprzedzają. Rzeczy, które uważamy za „główne otwarte problemy”, są rozwiązane i w rękach ludzi już dziś. Wystarczy wymienić kilka:

- LLM na telefonie: [Ludzie uruchamiają modele
podstawowe](https://twitter.com/thiteanish/status/1635678053853536256)
na Pixelu 6 z prędkością 5 tokenów / s.
- Skalowalna osobista sztuczna inteligencja: [Możesz dostroić
spersonalizowaną sztuczną inteligencję na swoim laptopie w jeden
wieczór](https://github.com/tloen/alpaca-lora).
- Odpowiedzialne wydanie: Ten nie jest „rozwiązany” tak bardzo, jak
„zbyteczny”. [Istnieją całkowicie bezpłatne strony internetowe pełne
modeli artystycznych](https://civitai.com/) bez żadnych ograniczeń, a
tekst [nie jest daleko w
tyle](https://medium.com/geekculture/list-of-open-sourced-fine-tuned-large-language-models-llm-8d95a2e0dc76).
- Multimodalność: [Obecny multimodalny SOTA ScienceQA został
wytrenowany w godzinę](https://arxiv.org/pdf/2303.16199.pdf).
  
Podczas gdy nasze modele nadal mają niewielką przewagę pod względem jakości, [różnica zamyka się zadziwiająco szybko](https://arxiv.org/pdf/2303.16199.pdf). Modele open source są szybsze, bardziej konfigurowalne, bardziej prywatne i na funt za funt bardziej zdolne. [Robią rzeczy za 100 USD i 13 mld parametrów](https://lmsys.org/blog/2023-03-30-vicuna/), z którymi mamy problemy za 10 mln USD i 540 mld. I robią to w tygodniach, a nie miesiącach. Ma to głębokie konsekwencje dla nas:
![Relative Response Quality Assessed by GPT-4](https://lmsys.org/images/blog/vicuna/chart.svg)
Nie mamy żadnego sekretnego sosu. Nasza najlepsza nadzieja to uczenie się i współpraca z tym, co robią inni poza Google. Powinniśmy priorytetowo traktować integracje 3P.
Ludzie nie będą płacić za ograniczony model, gdy darmowe, nieograniczone alternatywy są porównywalne jakościowo. Powinniśmy rozważyć, gdzie jest nasza wartość dodana.
Gigantyczne modele nas spowalniają. W dłuższej perspektywie najlepsze modele to te, które można szybko iterować. Powinniśmy uczynić małe warianty czymś więcej niż pochopnym pomysłem, teraz, gdy wiemy, co jest możliwe w reżimie <20B parametrów.

## Co się stało?

Na początku marca społeczność open source dostała w swoje ręce pierwszy naprawdę zdolny model bazowy, gdy LLaMA Meta wyciekła do opinii publicznej. Nie miał strojenia instrukcji ani rozmowy, ani RLHF. Niemniej jednak społeczność natychmiast zrozumiała znaczenie tego, co otrzymała.

Nastąpił ogromny wysyp innowacji, zaledwie kilka dni między głównymi wydarzeniami (zobacz Harmonogram dla pełnego podziału). Oto jesteśmy, ledwie miesiąc później, a są warianty z dostrojeniem instrukcji, kwantyzacją, poprawą jakości, ocenami ludzkimi, multimodalnością, RLHF itp. itp., z których wiele wzajemnie się uzupełnia.

Najważniejsze jest to, że rozwiązali problem skalowania w takim stopniu, że każdy może majstrować. Wiele nowych pomysłów pochodzi od zwykłych ludzi. Bariera wejścia do szkolenia i eksperymentowania spadła z całkowitego wyniku głównej organizacji badawczej do jednej osoby, jednego wieczoru i mocnego laptopa.


## Dlaczego mogliśmy się tego spodziewać?

Pod wieloma względami to nie powinno być zaskoczeniem dla nikogo. Obecny renesans w otwartych LLM nastąpił tuż po renesansie w generowaniu obrazów. Podobieństwa nie umknęły społeczności, wielu nazywa to „Stable Diffusion moment” dla LLM.

W obu przypadkach niskokosztowe zaangażowanie publiczne było możliwe dzięki znacznie tańszemu mechanizmowi dostrajania o nazwie niskorankowa adaptacja, lub LoRA, w połączeniu z przełomem w skali (latentna dyfuzja dla syntezy obrazu, Chinchilla dla LLM). W obu przypadkach dostęp do wystarczająco wysokiej jakości modelu rozpoczął lawinę pomysłów i iteracji ze strony osób i instytucji na całym świecie. W obu przypadkach szybko przewyższyło to dużych graczy.

Te wkłady były decydujące w obszarze generowania obrazów, ustawiając Stable Diffusion na inną ścieżkę niż Dall-E. Posiadanie otwartego modelu doprowadziło do integracji produktów, rynków, interfejsów użytkownika i innowacji, które nie miały miejsca w przypadku Dall-E.

Efekt był namacalny: szybka dominacja w dziedzinie wpływu kulturowego w porównaniu do rozwiązania OpenAI, które było zdominowane przez duże firmy. W ciągu kilku tygodni Stable Diffusion stał się de facto standardem w dziedzinie generowania obrazów, a Dall-E stał się ciekawostką historyczną. Czy to samo stanie się z LLM, pozostaje do zobaczenia, ale szerokie elementy strukturalne są już na miejscu.

# Co przegapiliśmy?

Innowacje, które napędziły ostatnie sukcesy open source, bezpośrednio rozwiązują problemy, z którymi nadal się borykamy. Większa uwaga na ich pracę mogłaby pomóc nam uniknąć wynajdywania koła.

### LoRA jest niesamowicie potężną techniką, na którą powinniśmy zwracać większą uwagę

LoRA działa poprzez reprezentowanie aktualizacji modelu jako faktoryzacji o niskim rzędzie, co zmniejsza rozmiar macierzy aktualizacji nawet kilkakrotnie. Pozwala to na dostrojenie modelu w ułamku kosztu i czasu. Możliwość spersonalizowania modelu językowego w kilka godzin na sprzęcie konsumenckim to duży sukces, zwłaszcza dla aspiracji, które obejmują włączenie nowej i różnorodnej wiedzy w czasie rzeczywistym. Fakt, że ta technologia istnieje, jest niedostatecznie wykorzystywana wewnątrz Google, chociaż bezpośrednio wpływa na niektóre z naszych najbardziej ambitnych projektów.

### Ponowne szkolenie modeli od podstaw to trudna droga

Częścią tego, co czyni LoRA tak skutecznym, jest to, że - podobnie jak inne formy dostrojenia - jest ono stosowalne. Ulepszenia, takie jak dostrojenie instrukcji, można zastosować, a następnie wykorzystać, gdy inni współpracownicy dodają dialog, rozumowanie lub narzędzia. Podczas gdy indywidualne dostrojenie jest niskorankowe, ich suma nie musi być, co pozwala na aktualizacje pełnego rzędu w przyszłości. 

Oznacza to, że w miarę pojawiania się nowych i lepszych zbiorów danych i zadań, model można tanio utrzymywać na bieżąco, bez konieczności ponoszenia kosztów pełnego uruchomienia.

W przeciwieństwie do tego, trenowanie dużych modeli od podstaw nie tylko odrzuca pre-trening, ale także wszelkie ulepszenia iteracyjne, które zostały wprowadzone na jego podstawie. W świecie open source nie trwa to długo, zanim te ulepszenia zdominują, sprawiając, że pełne ponowne szkolenie jest niezwykle kosztowne.

Powinniśmy rozważyć, czy każda nowa aplikacja lub pomysł naprawdę potrzebuje całkiem nowego modelu. Jeśli mamy naprawdę poważne ulepszenia architektoniczne, które uniemożliwiają bezpośrednie ponowne wykorzystanie wag modelu, powinniśmy zainwestować w bardziej agresywne formy destylacji, które pozwalają nam zachować jak najwięcej możliwości poprzedniej generacji.


### Duże modele nie są bardziej zdolne w dłuższej perspektywie, jeśli możemy szybciej iterować na małych modelach

Aktualizacje LoRA są bardzo tanie w produkcji (~100 USD) dla najpopularniejszych rozmiarów modeli. Oznacza to, że prawie każdy z pomysłem może wygenerować jeden i go rozpowszechniać. Czasy szkolenia poniżej jednego dnia są normą. Przy takim tempie nie trzeba długo, aby efekt kumulacyjny wszystkich tych dostrojeń przewyższył start z przewagą wielkości. W rzeczywistości, jeśli chodzi o godziny inżynierskie, tempo poprawy tych modeli znacznie przewyższa to, co możemy zrobić z naszymi największymi wariantami, a najlepsze są już w dużej mierze nie do odróżnienia od ChatGPT. Skupienie się na utrzymaniu niektórych z największych modeli na planecie faktycznie stawia nas w niekorzystnej sytuacji.

### Jakość danych skaluje się lepiej niż rozmiar danych

Wiele z tych projektów oszczędza czas, szkoląc się na małych, wysoko skomponowanych zbiorach danych. Sugeruje to pewną elastyczność w prawach skalowania danych. Istnienie takich zbiorów danych wynika z myślenia w linii Data Doesn't Do What You Think, a stają się one szybko standardowym sposobem szkolenia poza Google. Zbiory te są tworzone za pomocą metod syntetycznych (np. filtrowanie najlepszych odpowiedzi z istniejącego modelu) i szukania w innych projektach, z których żaden nie dominuje w Google. Na szczęście te zbiory danych wysokiej jakości są otwarte, więc można z nich korzystać za darmo.

### Bezpośrednia konkurencja z open source to przegrana propozycja

Najnowszy postęp ma bezpośrednie, natychmiastowe konsekwencje dla naszej strategii biznesowej. Kto zapłaci za produkt Google z ograniczeniami użytkowania, jeśli istnieje bezpłatna, wysokiej jakości alternatywa bez nich?

I nie powinniśmy oczekiwać, że będziemy w stanie nadrobić zaległości. Współczesny internet działa na open source z powodu pewnych znaczących zalet, których nie możemy powielić.

### Potrzebujemy ich bardziej niż oni nas potrzebują

Trzymanie naszej technologii w tajemnicy zawsze było wątpliwą propozycją. Badacze Google odchodzą do innych firm regularnie, więc możemy założyć, że wiedzą wszystko, co my wiemy, i będą nadal przez cały czas, dopóki ten potok nie zostanie zamknięty.

Ale trzymanie przewagi konkurencyjnej w technologii staje się jeszcze trudniejsze teraz, gdy najnowsze badania w zakresie LLM są przystępne cenowo. Instytucje badawcze na całym świecie budują na pracy innych, eksplorując przestrzeń rozwiązań w sposób szerokościowy, który daleko przewyższa nasze własne możliwości. Możemy próbować trzymać się mocno naszych sekretów, podczas gdy innowacje zewnętrzne rozmywają ich wartość, lub możemy próbować się od siebie uczyć.

### Osoby fizyczne nie są ograniczone licencjami w takim samym stopniu, jak korporacje

Wiele z tych innowacji dzieje się na podstawie wyciekłych wag modeli z Meta. Chociaż to nieuniknione się zmieni, gdy prawdziwie otwarte modele staną się lepsze, chodzi o to, że w międzyczasie osoby fizyczne mogą z nich korzystać w większym stopniu niż korporacje. Wystarczy spojrzeć na to, co się dzieje z GPT-3. Wszystkie najciekawsze aplikacje są tworzone przez osoby fizyczne, które korzystają z wycieków, a nie z licencjonowanych produktów. Jeśli chcemy mieć jakąkolwiek szansę na wykorzystanie tych innowacji, musimy je udostępnić w sposób, który umożliwia ich wykorzystanie przez osoby fizyczne.

### Bycie własnym klientem oznacza, że rozumiesz przypadek użycia

Przeglądając modele, które ludzie tworzą w przestrzeni generowania obrazów, można zauważyć ogromną ilość kreatywności, od generatorów anime po krajobrazy HDR. Modele te są używane i tworzone przez ludzi, którzy są głęboko zanurzeni w swoim konkretnym podgatunku, co daje głęboką wiedzę i empatię, której nie możemy mieć nadziei dorównać.

### Posiadanie ekosystemu: Pozwólmy Open Source pracować dla nas

Paradoksalnie, jedynym wyraźnym zwycięzcą w tym wszystkim jest Meta. Ponieważ wyciekły model był ich, skutecznie zgromadzili całą planetę darmowej pracy. Ponieważ większość innowacji open source dzieje się na podstawie ich architektury, nie ma nic, co mogłoby ich powstrzymać przed bezpośrednim włączeniem jej do ich produktów.

Wartość posiadania ekosystemu nie może być przeceniona. Sam Google z powodzeniem wykorzystał ten paradygmat w swoich ofertach open source, takich jak Chrome i Android. Posiadając platformę, na której dzieje się innowacja, Google cementuje się jako lider myśli i ustawiający kierunek, zdobywając zdolność kształtowania narracji na temat idei, które są większe niż on sam.

Im bardziej ściśle kontrolujemy nasze modele, tym bardziej atrakcyjne stają się otwarte alternatywy. Google i OpenAI obie zwróciły się obronnie ku wzorcom wydawniczym, które pozwalają im zachować ściślą kontrolę nad swoimi modelami, a jednocześnie pozwalają im na korzystanie z innowacji open source. To jest właśnie to, co musimy zrobić, aby wygrać.

Google powinien stać się liderem w społeczności open source, biorąc na siebie rolę lidera, współpracując zamiast ignorując szeroką rozmowę. Oznacza to prawdopodobnie podjęcie kilku niewygodnych kroków, takich jak publikowanie wag modeli dla małych wariantów ULM. Oznacza to konieczność zrezygnowania z kontroli nad tym, jak nasze modele są używane, ale to jest już fikcją. Każdy, kto chce używać LLM do nieautoryzowanych celów, może po prostu wybrać spośród dostępnych modeli.

## Epilog: A co z OpenAI?

Wszystkie te rozmowy na temat open source mogą wydawać się niesprawiedliwe wobec obecnej zamkniętej polityki OpenAI. Dlaczego musimy się dzielić, jeśli oni nie? Ale faktem jest, że już dzielimy się z nimi wszystkim w postaci stałego przepływu pochłoniętych starszych badaczy. Dopóki nie powstrzymamy tego przypływu, tajemnica jest bez znaczenia.

I w końcu OpenAI nie ma znaczenia. Popełniają te same błędy, co my, w swoim stosunku do open source, a ich zdolność do utrzymania przewagi jest koniecznie kwestionowana. Alternatywy open source mogą i w końcu ich przekroczą, chyba że zmienią swoje stanowisko. Przynajmniej w tym względzie możemy zrobić pierwszy krok.

## Harmonogram

24 lutego 2023 r. - LLaMA zostaje uruchomiona

Meta uruchamia LLaMA, udostępniając kod, ale nie wagi. W tym momencie LLaMA nie jest dostosowana do instrukcji ani rozmów. Podobnie jak wiele obecnych modeli, jest to stosunkowo mały model (dostępny w wersjach 7B, 13B, 33B i 65B parametrów), który został wytrenowany przez stosunkowo długi czas i jest więc dość zdolny w stosunku do swojego rozmiaru.

3 marca 2023 r. - Nieuniknione się dzieje

W ciągu tygodnia LLaMA wycieka do opinii publicznej. Wpływ na społeczność nie może być przeceniony. Istniejące licencje uniemożliwiają jego wykorzystanie w celach komercyjnych, ale nagle każdy może eksperymentować. Od tego momentu innowacje przychodzą ciężko i szybko.

12 marca 2023 r. - Modele językowe na tosterze

Niespełna tydzień później Artem Andreenko uruchamia model na Raspberry Pi. W tym momencie model działa zbyt wolno, aby był praktyczny, ponieważ wagi muszą być przekazywane do pamięci i z niej. Niemniej jednak to zapowiada lawinę wysiłków minifikacji.

13 marca 2023 r. - Dopasowanie na laptopie

Następnego dnia Stanford wydaje Alpaca, który dodaje dopasowanie instrukcji do LLaMA. Co ważniejsze niż faktyczne wagi, Eric Wang alpaca-lora repo, które wykorzystuje niski stopień dopasowania, aby szkolić „w ciągu kilku godzin na pojedynczym RTX 4090”.

Nagle każdy mógł dostosować model do dowolnego celu, rozpoczynając wyścig do dna w projektach dopasowania o niskim budżecie. Artykuły dumnie opisują swoje całkowite wydatki w wysokości kilkuset dolarów. Co więcej, aktualizacje o niskim stopniu można łatwo dystrybuować i oddzielnie od oryginalnych wag, co czyni je niezależnymi od oryginalnej licencji Meta. Każdy może je udostępniać i stosować.

14 marca 2023 r. - Teraz jest szybko

Georgi Gerganov używa kwantyzacji 4 bitów, aby uruchomić LLaMA na procesorze MacBooka. Jest to pierwsze rozwiązanie „bez GPU”, które jest wystarczająco szybkie, aby było praktyczne.

19 marca 2023 r. - Model 13B osiąga „parzystość” z Bardem

Następnego dnia współpraca międzyuniwersytecka wydaje Vicuna i wykorzystuje zasilany przez GPT-4 eval, aby zapewnić jakościowe porównania wyników modelu. Podczas gdy metoda oceny jest podejrzana, model jest istotnie lepszy niż wcześniejsze warianty. Koszt szkolenia: 300 USD.

Należy zauważyć, że mogli wykorzystać dane z ChatGPT, omijając ograniczenia jego API - po prostu próbkowali przykłady „imponującego” dialogu ChatGPT opublikowanego na stronach takich jak ShareGPT.

25 marca 2023 r. - Wybierz swój własny model

Nomic tworzy GPT4All, który jest zarówno modelem, jak i, co ważniejsze, ekosystemem. Po raz pierwszy widzimy modele (w tym Vicuna), które są gromadzone w jednym miejscu. Koszt szkolenia: 100 USD.

28 marca 2023 r. - Open Source GPT-3

Cerebras (nie mylić z naszym własnym Cerebra) szkoli architekturę GPT-3, wykorzystując optymalny harmonogram obliczeń wynikający z Chinchilla i optymalną skalę wynikającą z μ-parameterization. Przewyższa to istniejące klony GPT-3 o szerokim marginesie i stanowi pierwsze potwierdzone użycie μ-parameterization „w dziczy”. Modele te są szkolone od podstaw, co oznacza, że ​​społeczność nie jest już zależna od LLaMA.

28 marca 2023 r. - Wielomodalne szkolenie w ciągu godziny

Korzystając z nowej techniki Fine Tuning Parameter Efficient (PEFT), LLaMA-Adapter wprowadza dopasowanie instrukcji i wielomodalność w ciągu godziny szkolenia. Co więcej, robią to za pomocą zaledwie 1,2 miliona parametrów do nauczenia się. Model osiąga nowe SOTA w multimodalnym ScienceQA.

3 kwietnia 2023 r. - Prawdziwi ludzie nie mogą odróżnić 13B otwartego modelu od ChatGPT

Berkeley uruchamia Koala, model dialogowy szkolony wyłącznie za pomocą dostępnych bezpłatnie danych.

Podejmują kluczowy krok mierzenia rzeczywistych ludzkich preferencji między swoim modelem a ChatGPT. Podczas gdy ChatGPT nadal ma niewielką przewagę, ponad 50% użytkowników preferuje Koala lub nie ma preferencji. Koszt szkolenia: 100 USD.

15 kwietnia 2023 r. - RLHF Open Source na poziomach ChatGPT

Open Assistant uruchamia model i, co ważniejsze, zestaw danych dla Alignment via RLHF. Ich model jest blisko (48,3% vs. 51,2% na ChatGPT), ale ich zestaw danych jest znacznie większy i bardziej zróżnicowany. Koszt szkolenia: 100 USD.
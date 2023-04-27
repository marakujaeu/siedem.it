---
layout: post
title:  "Dlaczego system Windows 64-bitowy jest bezpieczniejszy od 32-bitowego?"
author: adam
categories: [ Porady ]
tags: [windows, Linux, MacOs, bezpieczeństwo]
description: "Dlaczego system Windows 64-bitowy jest bezpieczniejszy od 32-bitowego?"
featured: true
redirect_from:
  - /2013/11/08/dlaczego-system-64-bitowy-jest-bezpieczniejszy.html
  - /dlaczego-system-64-bitowy-jest-bezpieczniejszy.html
  - /adam/4-powody-dla-ktorych-64-bitowy-windows-jest-bezpieczniejszy-od-32-bitowego
---

**Jedną z najdziwniejszych rzeczy w temacie zabezpieczeń systemu [Windows](http://web.archive.org/web/20150514112826/http://siedem.it/tag/windows) jest to, że kilka z pozoru nieznaczących zmian w działaniu systemu może mieć znaczący wpływ na jego [bezpieczeństwo](http://web.archive.org/web/20150514112826/http://siedem.it/tag/bezpieczenstwo) i działanie złośliwego oprogramowania. Kto by przypuszczał, że 64-bitowy system sam w sobie utrudnia działanie złośliwego oprogramowania?**

Jak powiesz to jakiemuś samozwańczemu informatykowi, to prawdopodobnie wyśmieje Cię. Jest jednak kilka argumentów, które warto poznać, przemawiających za tym, że następnym razem dwa razy zastanowimy się nad instalacją 32-bitowego systemu operacyjnego.

Sterowniki są trudniejsze w obejściu
------------------------------------

Czasami złośliwe [oprogramowanie](http://web.archive.org/web/20150514112826/http://siedem.it/oprogramowanie) potrzebuje dostępu do jądra systemu operacyjnego. Aby tego dokonać stara się ono wstrzykiwać w sterowniki systemowe. Jeśli nie mamy zbyt dużej wiedzy w temacie sterowników, to warto przeczytać ten artykuł o ich działaniu. 64-bitowa [wersja systemu Windows](http://web.archive.org/web/20150514112826/http://siedem.it/adam/wersja-systemu-windows) wymaga certyfikowanych sterowników, co oznacza, że każdy bit kodu musi być zaakceptowany przez firmę [Microsoft](http://web.archive.org/web/20150514112826/http://siedem.it/tag/microsoft).

Czemu sterowniki 32-bitowe nie wymagają takiej certyfikacji? Głównie dlatego, że istnieje bardzo dużo starszych sterowników i z uwagi na ich ilość certyfikacja byłaby bardzo trudna. Twórcy 64-bitowych sterowników są świadomi wymagań i muszą dopilnować tego, by sterowniki były podpisywane certyfikatem. Oczywiście sterowniki napisane w późnych latach dziewiędziesiątych same nie podpiszą się w magiczny sposób. Więc jeśli korzystasz z 64-bitowej wersji systemu Windows, to jesteś znacznie bardziej zabezpieczonym użytkownikiem, a złośliwemu oprogramowaniu znacznie trudniej jest się dostać do jądra systemu. Są jeszcze inne powody, dla których 64-bitowy Windows jest bezpieczniejszy.

ASLR sprawia, że wprowadzenie złośliwego kodu do programu jest niemal niemożliwe
--------------------------------------------------------------------------------

Adress Space Layout Randomization (ASLR) to metoda przechowywania adresów do pamięci, z której korzysta program, w sposób nieprzewidywalny. W przypadku 32-bitowego systemu Windows niektóre programy rozpoczynają pracę zawsze z takim samym adresem, co znacznie ułatwia złośliwemu oprogramowaniu implementację złośliwego kodu. Chociaż nowe wersje systemu takie jak [Windows Vista](http://web.archive.org/web/20150514112826/http://siedem.it/tag/windows-vista), [Windows 7](http://web.archive.org/web/20150514112826/http://siedem.it/tag/windows-7) i [Windows 8](http://web.archive.org/web/20150514112826/http://siedem.it/tag/windows-8) również wykorzystują ASLR w 32-bitowych wersjach, to jest to narzędzie znacznie bardziej efektywne w przypadku 64-bitowego systemu. Im większy obszar pamięci, tym efektywniej nasze programy są chronione.

Zapobieganie wykonywaniu danych
-------------------------------

Oczywiście zarówno 32-bitowe jak i 64-bitowe systemy Windows posiadają Zapobieganie wykonywaniu danych (Data Execution Prevetion – DEP). Jednak w przypadku 64-bitowego systemu programy nie mogą ominąć tego mechanizmu. W przypadku 32-bitowego systemu DEP jest normalnie wyłączony, więc wykonanie danych w pamięci programów jest domyślnie możliwe. Wielu twórców złośliwego oprogramowania wykorzystują DEP do dodania paru linijek kodu na końcu pamięci programu, który w końcu zostanie wykonany. W ten sposób system może zostać z łatwością zainfekowany. Skoro w 64-bitowym systemie nie mamy możliwości ominięcia tego mechanizmu, to nie mamy problemu.

Powłoka WoW64
-------------

W folderze „Windows” możemy znaleźć podfolder, który nazywa się SysWOW64. Jest to nowa powłoka wymagana do wykonywania programów w 64-bitowym jądrze systemu. Nie jest to mechanizm stworzony do ochrony, ale po części pomaga on w tym, ponieważ aplikacje 32-bitowe nie mają bezpośredniego dostępu do jądra. Tak więc 32-bitowe złośliwe oprogramowanie nie będzie mogło wykonać kodu na 64-bitowym jądrze systemu. Ta sama powłoka jest również przyczyną niektórych 32-bitowych programów, które nie mogą działać na 64-bitowej wersji systemu Windows. Warto jednak zaznaczyć, że złośliwe oprogramowanie przystosowane do pracy w 64-bitowym jądrze systemu wciąż może zainfekować nasz komputer.

Podsumowanie
------------

64-bitowa wersja systemu Windows pozwala na dodatkowe zabezpieczenie przed złośliwym oprogramowaniem, nie oznacza to jednak, że jest całkowicie na nie odporne. Złośliwe oprogramowanie wciąż może wyrządzić wiele szkód, jeśli nie posiadamy dodatkowych zabezpieczeń. Opisywane przez mnie aspekty 64-bitowego oprogramowania w tym wpisie sprawiają trudności dla złośliwego oprogramowania, jakim są na przykład wirusy, robaki czy konie trojańskie. Jeżeli złośliwe oprogramowanie działa w trybie 32-bitowym, ale nie wykorzystuje do działania jądra systemu, wykonywania danych w pamięci programów czy też nie implementuje dodatkowego kodu do programów, to wciąż istnieje ryzyko infekcji. Przy następnej instalacji systemu operacyjnego warto jednak rozważyć instalację 64-bitowej wersji.
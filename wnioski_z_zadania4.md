# Porównanie podatności
Podatności znalezione podczas dynamicznej i statycznej
analizy podatności są fundamentalnie różne.

1. Analiza z Trivy czyli podatności znalezione w zależnościach aplikacji bibliotekach najbardziej odbiegają i nie mają wspólnego mianownika z pozostałymi testami. Pomagają znaleźć potencjalne podatności bezpieczeństwa wynikające z wynikających bibliotek w kontenerach dockerowych.
2. ZAP - znalazł bardzo małą w stosunku do pozostałych narzędzi ilość podatności przez analizę działającej aplikacji co pozwoliło na uniknięcie wykrycia wszyskich podatnosci które mogły by wynikać np z wykorzystania danej biblioteki ale nie są możliwe do wykorzystania przez brak wykorzystania konkretnej biblioteki.
3. Semgrep wykrył podatności które wynikały z samej implementacji elementów aplikacji co pozwala na najbardziej bezpośredni feedback dla developerów. Nie wykrywa jednak ani podatności dynamicznie ani bibliotek jak pozostałe.

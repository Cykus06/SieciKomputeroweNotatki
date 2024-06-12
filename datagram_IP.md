# Datagram IP

## Budowa datagramu IP

![Wizualizacja budowy datagramu IP](datagram_IP_budowa.png)

### Wersja protokołu IP

- Obecna wersja - 4
- Docelowo - IPv6 z m.in. 128 bitowym adresem oraz mechanizmami QoS

### Identyfikacja

Numer "seryjny" utworzonego przez nadawcę datagramu. Wraz jego adresem IP jednoznacznie identyfikuje każdy datagram w całym Internecie

### Czas życia Daragramu TTL

- Zmniejszany po każdym przejściu przez węzeł
- Zabezpiecza przed zapętleniem datagramu w sieci
- Użyteczny przy próbach śledzenia tracy (tracert)

### Suma kontrolna nagłowka

- Zabezpiecza przed pojedynczymi i seryjnymi błędami w nagłówku
- Prosty algorytm (suma modulo 2)

### Adresy

- Jednoznacznie identyfikują hosta w sieci
- Na podstawie adresu docelowego węzły pośredniczące dokonują wyboru drogi przesyłania datagramu przez sieć (next hop)

### Opcje nagłówka

- Rejestracja trasy i czasu przejścia przez węzły sieci
- Wymuszenie drogi routingu (swobodne lub dokładne)
- Ograniczenia dot. bezpieczeństwa

## Podział datagramu na fragmenty i ponowne składanie

Różne sieci skłądowe Internetu mają odmienne dopuszczalne formaty i długości jednostek danych protokołu sieciowego i datagram IP może być za długi. Zachodzi konieczność jego podziału na fragmenty, aby nie przekroczyć wielkości MTU (Maximum Transfer Unit).

![Wizualizacja budowy datagramu IP](datagram_IP_podzial.png)

- Datagram wysyłane z węzła A należy w bramie B1 dzielić na fragmenty o długości nie przekraczającej 1522 oktetów (np. 1156 oktetów).
- Każdy z fragmentów ma identyczny identyfikator ID (taki jak cały datagram). Fragmenty z wyjątkie ostatniego mają bit MF=1 (3-ci bit w polu FLAGS). W polu OFFSET każdy fragment ma wielkość przesunięcia względem początku pola danych Datagramu*


# TCP IP

ziór protokółów sieciowych, które są odpowiedzialne za komunikację między urządzeniami ("hostami") dołączonymi do dowolnych niejednorodnych sieci komputerowych, takich jak sieci rozległe **WAN** (np. publiczne sieci pakietowe X.25, FR, IP, ...), sieci satelitarne, sieci pakietowe komunikacji ruchomej (radiowe - mobile packets radio networks), (szybkie) sieci lokalne **LAN**.

Powyższe sieci traktuje się jako jedną wspólnotę (Internet), a protokoły TCP/IP są nazywane protokołami Internetu.

## Cechy wyróżniające usługi TCP/IP

### Niezależność od technologii

Protokoły TCP/IP definiują jednostkę danych (datagram) i określają reguły jego transmisji bez względu na technologię stosowaną w sieci.

### Zasięg światowy

Każdy komputer ma unikatowy adres. Każdy datagram ma w nagłówku parę adresów:

- komputera docelowego
- komputera źródłowego

Współpracować może dowolna para komputerów dołączonych do sieci (niezależnie od lokalizacji geograficznej).

### Potwierdzenia End-to-End

Potwierdzenia wymieniane są między komputerem docelowym i źródłowym.

### Zaimplementowane standardowe aplikacje

Protokoły TCP/IP zawierają standardy takie jak:

- poczta elektroniczna
- transfer zbiorów
- terminal wirtualny
- inne...

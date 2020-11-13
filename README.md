# go-vs-rust
Celem niniejszego wyzwania jest porównanie sprawności języków Go i Rust w dziedzinie tworzenia aplikacji HTTP. 
Wyzwanie z pozoru nie jest sprawidliwe, albowiem nie jest to główne przeznczenie języka Rust, jednak wielu twierdzi, że tego typu implementacje są proste w realizacji przy zastosowaniu odpowiedniego framework'a. Poza tym, jeżeli można takie rzeczy robić w C++, to dlaczego nie w rzeczoonym Rust skoro pretenduje on do miana następcy jeyka C++.
Zadanie polega na wykonaniu i udokumentowaniu następujących punktów:
1. Instalacja języka (kompilator i wszystkie potrzebne narzędzia) na komputerze programisty
2. Inicjalizacja projektu
3. Implementacja prostego serwisu HTTP, który zawiera:
- URL publiczny: `/`
- URL zabezpieczony przez `BasicAuth`: `/admin`
- URL serwujący zawartość statyczną: `/static`
- URL renderujący `HTML` z szablonu: `/render`
- URL do obsługi żądań `POST` z zawartością `application/json`: `/backend`
- URL do obsługi żądań `GET`  z parametrami: `/data?name=XXX&color=YYY`
- konfiguracja logera
4. Pobranie i instalacja wymaganych bibliotek 
5. Kompilacja lokalna
6. Crosskompilacja do nastęopujących architektur
- RaspberryPi
- amd64 na MacOS
- amd64 na Linux
- i386  na Windows
- amd64 na Windows

## Implementacja
Można wybrać dowolną platofrmę, wugodną dla osoby implementującej, lecz w dokumentacji należy ją wskazać

### Go
Realizowane w systemie operacyjnym Debian Buster
#### Ad. 1: Instalacja języka na komputerze programisty
```bash
wget https://golang.org/dl/go1.15.5.linux-amd64.tar.gz
tar -C /usr/local -xzf go1.15.5.linux-amd64.tar.gz
echo 'PATH=$PATH:/usr/local/go/bin' >> ~/.bashrc
source  ~/.bashrc
go version
```
#### Ad. 2: Inicjalizacja projektu
```bash
mkdir challenge
cd challenge/
go mod init challenge
```
#### Ad. 3: Implementacja prostego serwisu HTTP
```bash

```
#### Ad. 4: Pobranie i instalacja wymaganych bibliotek 
Nie ma potrzeby. 
Kompilator sam pobiera biblioteki na podstawie definicji w sekcji "import" w kodzie źródłowym. 
Informację o pobranych bibliotekach można znaleźć w pliku `go.mod`
```bash
cat go.mod
```
#### Ad. 5: Kompilacja lokalna
```bash
go build -o challenge main.go
```
#### Ad. 6: Cross-kompilacja
```bash
# Raspberry PI
GOOS=linux   GOARCH=arm GOARM=5 go build -o challenge_raspberry_arm5 main.go

# Linux amd64
GOOS=linux   GOARCH=amd64 go build -o challenge_linux_amd64  main.go

# MacOS amd64
GOOS=darwin  GOARCH=amd64 go build -o challenge_darwin_amd64 main.go

# Windows
GOOS=windows GOARCH=386   go build -o challenge_win_i386  main.go
GOOS=windows GOARCH=amd64 go build -o challenge_win_amd64 main.go
```

### Rust (todo)
Realizowane w systemie operacyjnym TODO
#### Ad. 1: Instalacja języka na komputerze programisty
```bash
TODO
```
#### Ad. 2: Inicjalizacja projektu
```bash
TODO
```
#### Ad. 3: Implementacja prostego serwisu HTTP
```bash
TODO
```
#### Ad. 4: Pobranie i instalacja wymaganych bibliotek 
```bash
TODO
```
#### Ad. 5: Kompilacja lokalna
```bash
TODO
```
#### Ad. 6: Cross-kompilacja
```bash
TODO
```

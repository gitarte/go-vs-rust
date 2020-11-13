# go-vs-rust
Celem niniejszego wyzwania jest porównanie sprawności języków Go i Rust w dziedzinie tworzenia aplikacji HTTP. 
Wyzwanie z pozoru nie jest sprawidliwe, albowiem nie jest to główne przeznczenie języka Rust, jednak wielu twierdzi, że tego typu implementacje są proste w realizacji przy zastosowaniu odpowiedniego framework'a. Poza tym, jeżeli można takie rzeczy robić w C++, to dlaczego nie w rzeczoonym Rust skoro pretenduje on do miana następcy jeyka C++.
Zadanie polega na wykonaniu i udokumentowaniu następujących punktów:
1. Instalacja języka na komputerze programisty
2. Inicjalizacja projektu
3. Implementacja prostego serwisu HTTP z:
- jednym URL'em publicznym:                                              "/"
- jednym URL'em zabezpieczonym przez BasicAuth:                          "/admin"
- jednym URL'em serwującym zawartość statyczną:                          "/static"
- jednym URL'em renderującym HTML z szablonu:                            "/render"
- jednym URL'em do obsługi ądań POST z zawartością `application/json`:   "/backend"
- jednym URL'em do obsługi ądań GET  z parametrami:                      "/data?name=XXX&color=YYY"
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

### Go

### Rust (todo)

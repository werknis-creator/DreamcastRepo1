# Dreamcast 3D Third-Person Game

Prosta gra 3D na Sega Dreamcast, zbudowana na KallistiOS (KOS).

## Sterowanie

| Przycisk             | Akcja                     |
|----------------------|---------------------------|
| Analog ←/→           | Obrót gracza              |
| Analog ↑/↓           | Chodzenie (przód/tył)     |
| X                    | Skok                      |
| START                | Wyjście z gry             |

## Kompilacja

Wymagane środowisko KallistiOS (KOS). Uruchom:

    make

Spowoduje to wygenerowanie pliku `game.elf`.

## Uruchamianie

### Emulator (Flycast, NullDC, Demul)
Użyj `dc-tool` lub przekonwertuj na obraz CDI:

    sh-elf-objcopy -O binary game.elf game.bin
    mkdcdisc -o game.cdi game.bin

### Prawdziwy sprzęt
Wgraj przez `dc-tool` (CODEROAD/BBA) lub wypal CDI na CD-R.

## Dostosowanie

Zmieniaj stałe na początku `main.c`:

- `GRAVITY`      — siła grawitacji
- `JUMP_FORCE`   — wysokość skoku
- `MOVE_SPEED`   — prędkość chodzenia
- `TURN_SPEED`   — prędkość obrotu
- `CAM_DISTANCE` — odległość kamery od gracza
- `CAM_HEIGHT`   — wysokość kamery nad graczem

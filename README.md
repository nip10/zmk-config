# Lily58 ZMK Config

Portuguese (PT-PT) QWERTY layout for a wireless Lily58 split keyboard running [ZMK firmware](https://zmk.dev/).

## Hardware

- **Board:** Mikoto 7.2 (nRF52840)
- **Display:** Nice!View
- **Firmware:** ZMK with ZMK Studio enabled

## Layout

### Base Layer

```
┌─────┬─────┬─────┬─────┬─────┬─────┐                    ┌─────┬─────┬─────┬─────┬─────┬─────┐
│ ESC │  1  │  2  │  3  │  4  │  5  │                    │  6  │  7  │  8  │  9  │  0  │BKSP │
├─────┼─────┼─────┼─────┼─────┼─────┤                    ├─────┼─────┼─────┼─────┼─────┼─────┤
│ TAB │  Q  │  W  │  E  │  R  │  T  │                    │  Y  │  U  │  I  │  O  │  P  │ DEL │
├─────┼─────┼─────┼─────┼─────┼─────┤                    ├─────┼─────┼─────┼─────┼─────┼─────┤
│CTRL │  A  │  S  │  D  │  F  │  G  │                    │  H  │  J  │  K  │  L  │  Ç  │ '/? │
│     │     │ ctrl│ alt │ cmd │     │                    │     │ ctrl│ alt │ cmd │     │     │
├─────┼─────┼─────┼─────┼─────┼─────┼──────┐    ┌───────┼─────┼─────┼─────┼─────┼─────┼─────┤
│SHIFT│  Z  │  X  │  C  │  V  │  B  │  +   │    │   º   │  N  │  M  │  ,  │  .  │  -  │SHIFT│
└─────┴─────┴─────┼─────┼─────┼─────┼──────┤    ├───────┼─────┼─────┼─────┼─────┴─────┴─────┘
                  │ OPT │ CMD │LOWER│SPACE │    │ ENTER │RAISE│BKSP │ CMD │
                  └─────┴─────┴─────┴──────┘    └───────┴─────┴─────┴─────┘
```

### Lower Layer (hold LOWER)

Symbols, dead keys for accents, F-keys, and Bluetooth.

```
┌─────┬─────┬─────┬─────┬─────┬─────┐                    ┌─────┬─────┬─────┬─────┬─────┬─────┐
│ F12 │ F1  │ F2  │ F3  │ F4  │ F5  │                    │ F6  │ F7  │ F8  │ F9  │ F10 │ F11 │
├─────┼─────┼─────┼─────┼─────┼─────┤                    ├─────┼─────┼─────┼─────┼─────┼─────┤
│     │  !  │  "  │  #  │  $  │  %  │                    │  &  │  /  │  (  │  )  │  =  │  ´  │
├─────┼─────┼─────┼─────┼─────┼─────┤                    ├─────┼─────┼─────┼─────┼─────┼─────┤
│     │  «  │  »  │  €  │  '  │  ?  │                    │  @  │  [  │  ]  │  {  │  }  │  ~  │
├─────┼─────┼─────┼─────┼─────┼─────┼──────┐    ┌───────┼─────┼─────┼─────┼─────┼─────┼─────┤
│     │BTCLR│ BT0 │ BT1 │ BT2 │ BT3 │      │    │       │  |  │  \  │  ;  │  :  │  _  │  *  │
└─────┴─────┴─────┼─────┼─────┼─────┼──────┤    ├───────┼─────┼─────┼─────┼─────┴─────┴─────┘
                  │     │     │     │      │    │       │     │ DEL │     │
                  └─────┴─────┴─────┴──────┘    └───────┴─────┴─────┴─────┘
```

### Raise Layer (hold RAISE)

Navigation, numbers, and F-keys.

```
┌─────┬─────┬─────┬─────┬─────┬─────┐                    ┌─────┬─────┬─────┬─────┬─────┬─────┐
│     │     │     │     │     │     │                    │     │     │     │     │     │     │
├─────┼─────┼─────┼─────┼─────┼─────┤                    ├─────┼─────┼─────┼─────┼─────┼─────┤
│     │  1  │  2  │  3  │  4  │  5  │                    │  6  │  7  │  8  │  9  │  0  │     │
├─────┼─────┼─────┼─────┼─────┼─────┤                    ├─────┼─────┼─────┼─────┼─────┼─────┤
│     │ F1  │ F2  │ F3  │ F4  │ F5  │                    │  ←  │  ↓  │  ↑  │  →  │ F6  │     │
├─────┼─────┼─────┼─────┼─────┼─────┼──────┐    ┌───────┼─────┼─────┼─────┼─────┼─────┼─────┤
│     │ F7  │ F8  │ F9  │ F10 │ F11 │      │    │       │HOME │PG_DN│PG_UP│ END │ F12 │     │
└─────┴─────┴─────┼─────┼─────┼─────┼──────┤    ├───────┼─────┼─────┼─────┼─────┴─────┴─────┘
                  │     │     │     │      │    │       │     │ DEL │     │
                  └─────┴─────┴─────┴──────┘    └───────┴─────┴─────┴─────┘
```

## Features

### Home Row Mods (Timeless)

Hold S/D/F or J/K/L to activate Ctrl/Alt/Cmd. Uses [timeless home row mods](https://zmk.dev/docs/keymaps/behaviors/hold-tap) configuration to prevent accidental triggers during fast typing:

- Only the **opposite hand** triggers the modifier hold
- 280ms tapping-term with `balanced` flavor
- `require-prior-idle-ms` ignores holds during fast typing bursts

### Portuguese Accents

Requires **macOS Portuguese input source** (System Settings > Keyboard > Input Sources > add "Portuguese").

| Accent | How to type |
|--------|-------------|
| á é í ó ú | Hold LOWER, tap `´`, release, tap vowel |
| ã õ | Hold LOWER, tap `~`, release, tap vowel |
| à | Hold LOWER, tap Shift+`´`, release, tap `a` |
| â ê ô | Hold LOWER, tap Shift+`~`, release, tap vowel |
| ç | Tap `Ç` key (right of L on base layer) |

### Bluetooth

On the LOWER layer (bottom-left):

| Key | Action |
|-----|--------|
| BTCLR | Clear current BT profile |
| BT0–BT3 | Select BT profile 0–3 |

## Flashing

1. Download the `firmware` artifact from [GitHub Actions](https://github.com/nip10/zmk-config/actions)
2. Connect a half via USB and **double-tap the reset button** to enter bootloader mode
3. Drag the matching `.uf2` file onto the USB drive that appears
4. Repeat for the other half (flash left side first)

## Building Locally

This config is built automatically via GitHub Actions on every push. The workflow uses the [ZMK build action](https://github.com/zmkfirmware/zmk/.github/workflows/build-user-config.yml).

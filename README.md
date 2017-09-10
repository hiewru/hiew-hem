# Hiew External Modules

- [Intro](#intro)
- [Setup](#setup)
- [Installation](#installation)
- [Usage](#usage)
- [HEM Collection](#hem-collection)
- [License](#license)

## Intro

[Hiew](Hiew.md) is a research and reverse-engineer toolkit for `Windows` (could be run on `Wine` in `macOS` or `Linux`).
Hiew could be extended by plugins, so called **H**iew **E**xternal **M**odules, `HEM`.

There is a collection of plugins released by various authors.

## Setup

At first you need to prepare `Hem` folder to place there new modules, then you need to specify that newly created folder in Hiew configuration file.

- **Create** `Hem` subfolder in `Hiew` **folder**.

  ```cmd
  >
  cd C:\Hiew
  mkdir Hem
  ```
- **Set** `Hem` **path** in `Hiew` config file `hiew8.ini`:
 ```cmd
  >
  notepad hiew8.ini
 ```
add option `HemPath` to `hiew8.ini`:
  ```ini
  [HiewIni 5.03]
  HemPath =   "C:\Hiew\Hem\"  ; Path to folder with Hiew External Modules
  ```

- Create `configuration file` with module [shortcuts](#shortcuts) for 'HEM' manager

 ```cmd
 >
 cd Hem
 echo [HemKeys 7.45]>hemkeys.ini
 ```

## Installation

For example, we have HEM named `Sample`, filename `Sample.hem`:

### Folder for plugins

- Create `Sample` subfolder in `Hem` folder (for ex. `Hiew\Hem\Sample`)

```cmd
cd C:\Hiew\Hem
mkdir Sample
```

### Install module

- Place `Sample.hem` in `Hiew\Hem\Sample` folder.

### Shortcuts

To add keyboard shortcut *(optional)*, add to `hemkeys.ini` in `Hem` folder:
```ini
[HemKeys 7.45]
s: Sample
```

Where:
- `s` - Shortcut, letter `s`
- `Sample` - name of the module as it's listed in HEM menu in `Hiew`


## Usage

Launch `Hiew`, press `F11` (`Hiew External Modules` menu), select and run (Enter) required module.
If you added shortcut as described [above](#shortcuts), you can just press F11, then assigned letter.
For the next time, previously selected module will be highlighted in the modules list.

### Menu navigation and HEM execution

- :arrow_up: and :arrow_down:, `Enter`
- `F11` - for quick run of previously executed module, so you could press `F11` twice to run last module again: `F11, F11`
- :abcd: `letter` - if you setup [shortcut](#shortcut) for module


## HEM Collection

See [Collection](Collection.md)

## License

Licenses of listed modules may not conform with repo license itself. Please, check licenses of corresponding modules.

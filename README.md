# TalkerApp

**Type, predict, speak.** TalkerApp is a desktop app for people who would rather type than talk. You write — slowly, with one finger, a switch or eye gaze — the app suggests the next words, and a voice says it out loud. It works offline, needs no account and sends no telemetry.

### [⬇ Download the latest version](https://github.com/LukaszCzerwinski/TalkerApp/releases/latest)

[gettalker.app](https://gettalker.app) · [Po polsku ↓](#po-polsku)

This repository holds the installers only. TalkerApp is closed source: the "Source code" archives GitHub adds to every release contain nothing but this page.

## Which file do I need?

| Your computer | File |
|---|---|
| Mac with Apple silicon (M1 or newer) | `TalkerApp_<version>_aarch64.dmg` |
| Windows 10 or 11, 64-bit | `TalkerApp_<version>_x64-setup.exe` (about 22 MB) |
| Windows without an internet connection | `TalkerApp_<version>_x64-setup-offline.exe` (about 280 MB — it carries the Microsoft WebView2 component) |

Macs with an Intel processor are not supported by these builds. Local AI models need memory: the medium ones 8 GB of RAM, the largest 16 GB. Writing, prediction and the system voice work on any supported computer.

## Installation

### macOS

1. Open the `.dmg` file and drag **TalkerApp** into **Applications**.
2. Open TalkerApp from Applications.
3. If macOS says Apple could not verify the app, open **System Settings → Privacy & Security**, scroll to **Security** and click **Open Anyway** next to TalkerApp. Enter your password. The button stays for about an hour after you tried to open the app; if it has gone, open TalkerApp again. After that a normal double-click is enough.

TalkerApp is not yet signed with an Apple developer certificate, which is why macOS asks. Until it is, macOS treats each new version as a new app: after an update it may ask again for Keychain access (where your API keys are stored) and for the microphone and Accessibility permissions. Choose "Always Allow".

### Windows

1. Run the installer. It does not need administrator rights.
2. If a blue **Windows protected your PC** window appears (SmartScreen), click **More info**, then **Run anyway**. Windows shows it for programs it does not know yet.
3. TalkerApp needs Microsoft Edge WebView2. It is part of Windows 11 and most Windows 10 computers. If it is missing, the regular installer downloads it; the offline installer has it inside.

### Updating

TalkerApp does not update itself yet. Download the new version from this page and install it the same way. Your settings, phrases, history, downloaded models and API keys stay where they are.

## Check your download

Every release is immutable: once published, its files and its tag cannot be changed, and GitHub signs a record of each file. With the [GitHub CLI](https://cli.github.com):

```bash
gh release verify-asset <tag> <file> -R LukaszCzerwinski/TalkerApp
```

Without it, compare the file's SHA-256 with the line in `SHA256SUMS.txt` on the release page:

- macOS: `shasum -a 256 TalkerApp_<version>_aarch64.dmg`
- Windows (PowerShell): `Get-FileHash .\TalkerApp_<version>_x64-setup.exe`

The `*.cdx.json` files are software bills of materials (CycloneDX): the list of components in that build.

## Free and Pro

The Free edition never expires. Pro adds every cloud voice with emotion, the keyboard that types into other apps, personas with style learning and the multi-voice Recording Studio. It is a 12-month licence for two computers that does not renew by itself — see [gettalker.app](https://gettalker.app).

## Help and contact

Public issues are switched off on purpose: a bug report from a communication app easily contains private conversations. Write to **hello@gettalker.app** instead. If something does not work, attach the report from **Settings → Diagnostics → Save diagnostics report** — it leaves out your API keys and what you typed.

Security vulnerabilities: see [SECURITY.md](SECURITY.md).

## Licence

© 2026 OneFinger – Łukasz Czerwiński. TalkerApp is proprietary software; all rights reserved. The open-source components it uses and their licences are listed in the app under **Settings → Advanced → Open-source licences**.

---

## Po polsku

**Piszesz, aplikacja podpowiada i mówi.** TalkerApp to aplikacja na komputer dla osób, którym łatwiej pisać niż mówić. Piszesz — powoli, jednym palcem, przełącznikiem albo wzrokiem — aplikacja podpowiada kolejne słowa, a głos czyta tekst na głos. Działa bez internetu, nie wymaga konta i nie wysyła telemetrii.

### [⬇ Pobierz najnowszą wersję](https://github.com/LukaszCzerwinski/TalkerApp/releases/latest)

To repozytorium zawiera tylko instalatory. Kod TalkerApp jest zamknięty: archiwa „Source code”, które GitHub dodaje do każdego wydania, zawierają wyłącznie tę stronę.

### Który plik pobrać?

| Twój komputer | Plik |
|---|---|
| Mac z procesorem Apple (M1 lub nowszy) | `TalkerApp_<wersja>_aarch64.dmg` |
| Windows 10 lub 11, 64-bitowy | `TalkerApp_<wersja>_x64-setup.exe` (ok. 22 MB) |
| Windows bez dostępu do internetu | `TalkerApp_<wersja>_x64-setup-offline.exe` (ok. 280 MB — zawiera składnik Microsoft WebView2) |

Maki z procesorem Intel nie są obsługiwane przez te wersje. Lokalne modele AI potrzebują pamięci: średnie 8 GB RAM, największe 16 GB. Pisanie, podpowiedzi i głos systemowy działają na każdym obsługiwanym komputerze.

### Instalacja

**macOS**

1. Otwórz plik `.dmg` i przeciągnij **TalkerApp** do folderu **Programy**.
2. Otwórz TalkerApp z folderu Programy.
3. Jeśli macOS napisze, że Apple nie może zweryfikować aplikacji, otwórz **Ustawienia systemowe → Prywatność i ochrona**, przewiń do sekcji o zabezpieczeniach i kliknij **Otwórz mimo to** przy informacji o TalkerApp. Podaj hasło do konta. Przycisk jest dostępny przez około godzinę od próby otwarcia; jeśli zniknął, otwórz TalkerApp jeszcze raz. Potem wystarczy zwykłe dwukrotne kliknięcie.

TalkerApp nie ma jeszcze certyfikatu dewelopera Apple i dlatego macOS pyta. Do tego czasu każda nowa wersja jest dla systemu nową aplikacją: po aktualizacji może znowu poprosić o dostęp do Pęku kluczy (tam są Twoje klucze API) oraz o zgodę na mikrofon i Dostępność. Wybierz „Zawsze pozwalaj”.

**Windows**

1. Uruchom instalator. Nie potrzebuje uprawnień administratora.
2. Jeśli pojawi się niebieskie okno **System Windows ochronił ten komputer** (SmartScreen), kliknij **Więcej informacji**, a potem **Uruchom mimo to**. Windows pokazuje je przy programach, których jeszcze nie zna.
3. TalkerApp potrzebuje składnika Microsoft Edge WebView2. Jest częścią Windows 11 i większości komputerów z Windows 10. Jeśli go brakuje, zwykły instalator pobierze go z internetu, a instalator offline ma go w środku.

**Aktualizacja**

TalkerApp nie aktualizuje się jeszcze sama. Pobierz nową wersję z tej strony i zainstaluj ją tak samo. Ustawienia, frazy, historia, pobrane modele i klucze API zostają na miejscu.

### Sprawdzenie pobranego pliku

Każde wydanie jest niezmienne: po publikacji nie da się podmienić jego plików ani etykiety, a GitHub podpisuje zapis każdego pliku. Z [GitHub CLI](https://cli.github.com):

```bash
gh release verify-asset <etykieta> <plik> -R LukaszCzerwinski/TalkerApp
```

Bez niego porównaj skrót SHA-256 pliku z wierszem w `SHA256SUMS.txt` na stronie wydania:

- macOS: `shasum -a 256 TalkerApp_<wersja>_aarch64.dmg`
- Windows (PowerShell): `Get-FileHash .\TalkerApp_<wersja>_x64-setup.exe`

Pliki `*.cdx.json` to wykazy składników oprogramowania (CycloneDX) danej wersji.

### Free i Pro

Wersja Free nie wygasa. Pro dodaje wszystkie głosy z chmury z emocjami, klawiaturę piszącą w innych aplikacjach, persony z nauką stylu i wielogłosowe Studio nagrań. To licencja na 12 miesięcy na dwa komputery, która sama się nie odnawia — szczegóły na [gettalker.app](https://gettalker.app).

### Pomoc i kontakt

Publiczne zgłoszenia są celowo wyłączone: zgłoszenie błędu z aplikacji do komunikacji łatwo zawiera prywatne rozmowy. Napisz na **hello@gettalker.app**. Jeśli coś nie działa, dołącz raport z **Ustawienia → Diagnostyka → Zapisz raport diagnostyczny** — nie ma w nim kluczy API ani Twoich tekstów.

Luki bezpieczeństwa: zobacz [SECURITY.md](SECURITY.md).

### Licencja

© 2026 OneFinger – Łukasz Czerwiński. TalkerApp jest oprogramowaniem własnościowym; wszelkie prawa zastrzeżone. Komponenty open source i ich licencje są wymienione w aplikacji w **Ustawienia → Zaawansowane → Licencje open source**.

# Nextpad

Free native code editor for Mac. Nextpad opens, edits, and saves source files with syntax highlighting, tabs, and right-to-left text. It is built for people who write code on macOS and want a fast editor with no subscription.

Nextpad is free software under the [GNU General Public License v3.0](LICENSE). There is no account, no telemetry, and no upload of your files.

## Install

1. Download [Nextpad.dmg](dist/Nextpad.dmg), or the latest file from [Releases](https://github.com/Binhanaa/Nextpad/releases).
2. Open the disk image.
3. Drag **Nextpad** to **Applications**.
4. Open Nextpad from Applications or Spotlight.

macOS 11 or later. Apple silicon and Intel.

## What it is for

- Edit source in a native window: Swift, C, C++, Objective-C, Python, JavaScript, PHP, HTML, CSS, JSON, XML, shell, and many more.
- Keep several files open in tabs and restore the session.
- Search and replace, including regular expressions.
- Fold code with a simple margin that stays readable in both text directions.
- Write Arabic and other right-to-left text. The scrollbar moves to the left, and selection follows the word you click.
- Change the font size of the current file without resizing every open tab.

## Privacy

Nextpad does not have an account and does not send the contents of your files anywhere. Preferences, backups, and the session stay in `~/Library/Application Support/Nextpad++` on this Mac. An optional update check only asks GitHub whether a newer release exists. It does not include your documents.

## Build

The editor is Objective-C++ and C++, with Scintilla and Lexilla. CMake 3.20 or later and Xcode are required.

```sh
cmake -S . -B build -DCMAKE_BUILD_TYPE=Release
cmake --build build --target NotepadPlusPlusMac -j 8
```

The app is `build/Nextpad.app`.

Headless search tests:

```sh
cmake -S . -B build-release -DCMAKE_BUILD_TYPE=Release
cmake --build build-release --target npp_tests -j 8
ctest --test-dir build-release --output-on-failure
```

## Contributing

Issues and pull requests are welcome. Please open an issue before a large change.

1. Fork the repository.
2. Create a branch from `main`.
3. Keep the change focused and describe how you tested it.
4. Open a pull request.

By contributing, you agree that your contribution is licensed under GPL-3.0.

## License and credit

Nextpad is distributed under GPL-3.0, the same license as [Notepad++](https://notepad-plus-plus.org).

- **Don Ho** — original author of Notepad++.
- **Andrey Letov** — macOS port that this project continues.
- **Scintilla** and **Lexilla** — the editing component and lexers.

This project is not affiliated with the Notepad++ team.

Locale Emulator
===============

[![license](https://img.shields.io/github/license/xupefei/Locale-Emulator.svg)](https://www.gnu.org/licenses/lgpl-3.0.en.html)
[![AppVeyor](https://img.shields.io/appveyor/ci/xupefei/Locale-Emulator.svg)](https://ci.appveyor.com/project/xupefei/Locale-Emulator)
[![Github All Releases](https://img.shields.io/github/downloads/xupefei/Locale-Emulator/total.svg)](https://github.com/xupefei/Locale-Emulator/releases)
[![GitHub release](https://img.shields.io/github/release/xupefei/Locale-Emulator.svg)](https://github.com/xupefei/Locale-Emulator/releases/latest)

Yet Another System Region and Language Simulator

![LE interface](https://i.imgur.com/E4Gqyly.png)

## Download ##

Download available at <https://github.com/xupefei/Locale-Emulator/releases>.

For usage, please read <https://xupefei.github.io/Locale-Emulator/> (in English and 中文).

## Translate ##

If you want to help translating Locale Emulator, you can find all strings in

 -  `DefaultLanguage.xaml` in `LEGUI/Lang` folder.
 -  `DefaultLanguage.xml` in `LEContextMenuHandler/Lang` folder.

After you translated the above files into your language, please inform me by creating a pull request.

## Build ##

 1. Clone the repo using Git.
 2. Install Microsoft Visual Studio 2015 / 2017.
 3. Open `LocaleEmulator.sln`.
 4. Perform Build action.
 5. Clone and build the core libraries: https://github.com/xupefei/Locale-Emulator-Core (archived; see below)
 6. Copy LoaderDll.dll and LocaleEmulator.dll next to LEProc.exe in the build output folder (for example `Build\Debug` or `Build\Release`).

### Core DLLs ###

`LoaderDll.dll` and `LocaleEmulator.dll` are not part of this repository. They are the native, x86-only
injection/hooking core and live in the separate
[Locale-Emulator-Core](https://github.com/xupefei/Locale-Emulator-Core) repository, which has been archived
since April 2022. The managed solution here does not build them, so a fresh build has no core DLLs and
`LEProc` shows the "Some of the core Dlls are missing" message.

You can get them by:

- building `LoaderDll` and `LocaleEmulator` (Win32 configuration) from Locale-Emulator-Core. That requires
  Visual Studio 2013/2015 and the legacy WDK 7.1/8.0 and patched linker bundled in that repository; or
- extracting them from an official Locale Emulator release (for example the 2.5.0.0 ZIP); or
- copying them from an existing working Locale Emulator installation.

Place both files next to `LEProc.exe`. They are 32-bit only: Locale Emulator does not support x64 or ARM64
targets.

## License ##

![LGPL](https://www.gnu.org/graphics/lgplv3-147x51.png)

`LEContextMenuHandler` project use source codes from [Microsoft All-In-One Code Framework](https://blogs.msdn.com/b/onecode/) which is licensed by [Microsoft Public License](https://www.microsoft.com/en-us/openness/licenses.aspx#MPL).

[Flat icon set](commit/eae9fbc27f1a4c85986577202b61742c6287e10a) from [graphicex](https://graphicex.com/icon-and-logo/15983-flat-alphabet-in-9-colors-with-long-shadow-6913875.html).

All other source code files are licensed under [LGPL-3.0](https://opensource.org/licenses/LGPL-3.0).

If you want make any modification on these source codes while keeping new codes not protected by LGPL-3.0, please contact me for a sublicense instead.

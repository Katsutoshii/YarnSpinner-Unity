# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added

- Added a 3D speech bubble sample, for dynamically positioning a speech bubble above a game character. (@radiatoryang)
- Added a phone chat sample. (@radiatoryang)
- Added a visual novel template. (@radiatoryang)
- Added support for voice overs. (@Schroedingers-Cat)
- Added a dedicated voice over example scene which supports Unity's audio system and FMOD (@Schroedingers-Cat)
- Added voice overs to the space ship example scene (Stefanie Enge and @Schroedingers-Cat)
- Added a new API for presenting and managing lines of dialogue.
- Added an option to DialogueUI to allow hiding character names.
- The Yarn Spinner Window (Window -> Yarn Spinner) now shows the current version of Yarn Spinner.

### Changed

- Nicer error messages when the localized text for a line of dialogue can't be found.
- DialogueUI is now a subclass of DialogueViewBase. (@desplesda and @Schroedingers-Cat)
- Moved Yarn Spinner classes into the `Yarn.Unity` namespace, or one of its children, depending on its purpose.

### Removed

## [v1.2.6]

Note: Versions 1.2.1 through 1.2.5 are identical to v1.2.0; they were version number bumps while we were diagnosing an issue in OpenUPM.

### Changed

- Fixed compiler issues in Unity 2019.3 and later by adding an explicit reference to YarnSpinner.dll in YarnSpinnerTests.asmdef

## [v1.2.0] 2020-05-04

This is the first release of v1.2.0 of Yarn Spinner for Unity as a separate project. Previously, this project's source code was part of the Yarn Spinner repository. Version 1.2.0 of Yarn Spinner contains an identical release to this.

### Added

- Yarn scripts now appear with Yarn Spinner icon. (@Schroedingers-Cat)
- Documentation is updated to reflect the current version number (also to mention 2018.4 LTS as supported)
- Added a button in the Inspector for `.yarn` files in Yarn Spinner for Unity, which updates localised `.csv` files when the `.yarn` file changes. (@stalhandske, https://github.com/YarnSpinnerTool/YarnSpinner/issues/227)
- Added handlers for when nodes begin executing (in addition to the existing handlers for when nodes complete.) (@arendhil, https://github.com/YarnSpinnerTool/YarnSpinner/issues/222)
- `OptionSet.Option` now includes the name of the node that an option will jump to if selected.
- Added unit tests for Yarn Spinner for Unity (@Schroedingers-Cat)
- Yarn Spinner for Unity: Added a menu item for creating new Yarn scripts (Assets -> Create -> Yarn Script)
- Added Nuget package definitions for [YarnSpinner](http://nuget.org/packages/YarnSpinner/) and [YarnSpinner.Compiler](http://nuget.org/packages/YarnSpinner.Compiler/).

### Changed

- Fixed a crash in the compiler when parsing single-character commands (e.g. `<<p>>`) (https://github.com/YarnSpinnerTool/YarnSpinner/issues/231)
- Parse errors no longer show debugging information in non-debug builds.
# Fire and Reform DE

Launcher-ready **Definitive Edition Beta 1.0** payload for the original **Age of Empires III: The Asian Dynasties**, by Miracle Studio.

Original project: [Fire and Reform on ModDB](https://www.moddb.com/mods/fire-and-reform).

This Chinese-language total conversion covers the Renaissance through the Thirty Years War, with factions from Europe, Asia and Africa. Vietnam and Songhai are disabled in this beta, as described in the original readme. The mod's “Definitive Edition” name refers to this mod release; its engine is the original AoE3:TAD.

## Download and installation

Download [FireAndReform-beta1.0-win11.zip](https://github.com/Gorgorito12/Fire-and-Reform/releases/download/beta1.0/FireAndReform-beta1.0-win11.zip), or use [AoE3 Mod Launcher](https://github.com/Gorgorito12/AoE3-Mod-Launcher).

Requires your own installed copy of Age of Empires III: The Asian Dynasties. The launcher clones that installation into a separate folder and applies this mod overlay. It uses a private setup registry key and a separate `My Games\Fire and Reform DE` save folder.

The ZIP contains 8,240 files, with mod files at its root. Unmodified files already supplied by the reference base game were omitted by the launcher's `package-mod-payload.ps1`; the supplied compiled XML files were preserved.

SHA-256:

```text
8872192388310f416a8d63f52561f811773b43c3bb1fefc0f9213bd939ba7d6f  FireAndReform-beta1.0-win11.zip
```

## Windows compatibility changes

This payload differs from the original packaged mod in exactly two entries:

- `UHC.dll`: replaced with the version used by Wars of Liberty (1,187,840 bytes; SHA-256 `c070d138c2b4ead70ef07f44dae57a6667ffc53b59a178ddade39db48e01efb2`).
- `Startup/uhc.cfg`: `noAILimit` changed to `noAILimitV2`. Every other configuration line is preserved.

The original combination crashed before the menu on the tested Windows 11 machine with exception `0xe06d7363`. With these two changes the game log reported startup complete in 15.93 seconds. The maintainer accepted this result; a skirmish and canonical-peer multiplayer compatibility have **not** been verified. The launcher applies the private registry-key patch only to each player's local executable at installation time.

## Provenance

- Source archive: `beta1.0.rar`, from the original ModDB project.
- Source archive SHA-256: `9db67d1396a9fca3d529d8bd8664bc4c6bbb835b38386f761441e48257709f2f`.
- All mod/game assets and their rights remain with their respective authors. This repository provides a community-maintained launcher package.

## En español

Paquete de **Fire and Reform Definitive Edition Beta 1.0**, en chino, para el AoE3:TAD original. Requiere tu propia instalación del juego. El launcher lo instala en una carpeta separada y aísla sus guardados. Incluye UHC actualizado y `noAILimitV2`; el registro confirmó el arranque, pero no se completaron pruebas de escaramuza ni de compatibilidad multijugador con instalaciones originales.

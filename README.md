# MVTaikoChecks

A set of osu!taiko specific [Mapset Verifier](https://github.com/Naxesss/MapsetVerifier) checks

> [!WARNING]
> This plugin is still in heavy development, so [false positives and false negatives](https://en.wikipedia.org/wiki/False_positives_and_false_negatives) may occur. If you find something that isn't right, please refer to the *[Feature requests & bug reports](#feature-requests--bug-reports)* section.
>
> **ALWAYS APPLY YOUR OWN JUDGEMENT ON EVERY CHECK AND DON'T BLINDLY FOLLOW THEM.**

## Features

### BPM scaling

Checks try to compensate for BPM scaling when needed, however this is not perfect and may cause false positives in very high or low BPM maps. **Always use your manual judgement with every check.**

| BPM | Action |
| :-- | :-- |
| BPM <= 110 | effective BPM is multiplied by 2 |
| 110 < BPM <= 130 | effective BPM multiplied by 1.5 |
| 130 < BPM < 270 | effective BPM is unchanged |
| BPM >= 270 | effective BPM is divided by 2 |

> [!IMPORTANT]
> This unfortunately **does not** work on double/half BPM-style maps that don't change the actual BPM value, so it will cause false positives.

### Available checks

- Double barlines
- Rest moments
- Unrankable finishers
- Abnormal note gaps
- Spinner gap
- OD/HP settings
- Kiai flashes
- Unsnapped last note that accidentally hides its barline
- Pattern lengths
- Inconsistent kiai toggles across difficulties
- Barlines unaffected by SV when they likely should be

### Planned checks

- Extreme SV changes/SV jumps in lower difficulties

## Installing

1. Download and install Mapset Verifier from [here](https://github.com/Naxesss/MapsetVerifier#download) if you don't have it already
2. Download the [latest release](https://github.com/Hiviexd/MVTaikoChecks/releases/latest) of `MVTaikoChecks.dll`
3. Open MV and click the settings icon (top right)
4. Scroll down to the `Shortcuts` section
5. Click the `Open externals folder` icon
6. Open the `checks` folder
7. Close MV and place the `MVTaikoChecks.dll` file in the folder above
8. Start MV again

## Known issues

Difficulties with custom names are always marked as "Easy" so make sure you manually change that to the correct diff, else you'll have an insane amount of flase positives.

> [!NOTE]
> This is an issue with Mapset Verifier (specifically the lack of osu!taiko SR calculation), not this plugin.

https://github.com/Hiviexd/MVTaikoChecks/assets/62819481/55cdb56d-0c25-4dda-8ed3-af472361f1dd

## Feature requests & bug reports

If you have any feature requests or an issue to report, please open an issue or reach out to one of the active maintainers below:

- **Hivie** (osu!: [Hivie](https://osu.ppy.sh/users/14102976) | Discord: `hivie`)
- **Nostril** (osu!: [Nostril](https://osu.ppy.sh/users/11479122) | Discord: `nostril`)

## Contributing

If you're here to contribute, please open an issue to discuss your idea before you start working on it.

### Special thanks

- [phob144](https://github.com/phob144) for being integral to development in early stages

<!-- 
## Notes

[^note-unstable]: This check is currently unstable and may cause false positives.
-->

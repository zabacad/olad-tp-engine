# Of Light and Darkness: The Prophecy — Engine reimplementation

> Prophets have said that life, as we know it, will end on May 5, 2000.
> According to these prophecies, the final battle between the forces of light
> and darkness has already begun.
>
> — Angel Gemini (From the CD case.)

*Of Light and Darkness: The Prophecy* is a 1998 action adventure game for
Windows 95. It was published by Interplay Productions (now Interplay
Entertainment), and was the only game developed under the Tribal Dreams brand.
Little information about the game available on the Internnet. The
[Wikipedia entry][wiki] was not created until 2017. At least one recorded
playthrough is available on YouTube.

Reviews are mixed and sometimes negative, noting initial confusion followed by
repetitiveness. The game does exhibit a unique and bold visual style. The
environment can be described as otherworldly and spooky.

The goal of this project is to reimplement the game engine for modern
computers. Given the original data files, it should allow the game to be played
without such outdated technology as Windows 95, an optical drive, or a forced
screen resolution.

[wiki]: https://en.wikipedia.org/wiki/Of_Light_and_Darkness:_The_Prophecy

## Project phases

1. Determine and document the layout of the game disks and installation
directory and the purpose of each set of data files.

2. For each type of data file, determine and document its naming scheme,
structure, layout, and format.

3. Write parsers for these data files and programs to display and explore the
parsed data.

4. Create an engine that replicates gameplay behaviour and integrate the
parsers into it.

## Gameplay technical overview

The game environment was modeled in 3D and rendered into a series of images and
animations. Each location is presented as a panorama which is rotated by moving
the mouse cursor near the left and right edges of the screen. Several panoramas
include animation. Interaction and movement is by clicking on hotspots in the
panoramas. Movement between locations is shown with a full screen video.
Occationally, there is a static view up or down, accessed by clicking near the
top or bottom on the screen. Removable objects appear superimposed at fixed
locations in each panorama. The mouse cursor is animated and context sensitive.
The game menu appears in the same manner as one of these locations.

All locations and transitions are loaded from the optical media, which is a set
of three compact discs.

The spacebar opens the inventory while held. It appears at the top of the
screen, with the game paused behind it in greyscale.

Most locations include looping background audio, and most actions include an
associated audio cue. There is also an announcer at times.

The original engine was called the EDEN Engine and was developed by Heartland
Enterprises. The game was designed for Windows 95, but also appears to work on
64-bit Windows 8.

The game was re-released on [Good Old Games][gog] in 2016.

[gog]: https://www.gog.com/game/of_light_and_darkness_the_prophecy

## CD contents

### Disc 1 (CD-C95-166-0)

Game files:

- `CURSORS` — `*.ICO` files appear to be in-game cursors, which are color and
  animated. Unknown format (not Windows icon). Appear compressed.
- `FONTS` — `ENG16.TGA`, `ENG24.TGA`, `NOS4R2.TGA`. Targa font files. Letters
  arranged vertically.
- `IBMS` — `IBMS2.TGA`. Targa image of every inventory item arranged
  vertically. Normal and picked states.
- `MANUAL` — `MANUAL.PDF`. PDF manual. Note there is no physical manual
  included with the game.
- `MOVIES` — `*.MVE`. Interplay format readable by ffmpeg. All fullscreen
  videos. Several cutscenes.
  - `##A_##A.MVE` — Transitions from one location to another. Numbers likely
    location identifiers.
- `SAVE` — Empty.
- `TRACKS` — Three uncompressed audio files with RIFF magic number.
  - `DROID01.SND` — Menu music.
- `VIDEOS` — `*.VID`. Interplay format readable by ffmpeg, but appear with the
  top left. Partial-screen videos, including audio.

Other:

- `DEMOS` — Demos and trailers for other Interplay games.
- `DIRECTX` — DirectX 4 redistributable.
- `EREG` — Electronic registraion.
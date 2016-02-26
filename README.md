# Of Light and Darkness: The Prophecy -- Engine reimplementation

> Prophets have said that life, as we know it, will end on May 5, 2000.
> According to these prophecies, the final battle between the forces of light
> and darkness has already begun.
>
> -- Angel Gemini (From the CD case.)

*Of Light and Darkness: The Prophecy* was a 1998 action adventure game for
Windows 95. It was published by Interplay Productions (now Interplay
Entertainment), and was the only game developed under the Tribal Dreams brand.

Reviews are mixed and sometimes negative, noting initial confusion followed by
repetitiveness. The game does exhibit a unique and bold visual style. The
environment can be described as otherworldly and spooky.

Little information is available about the game other than reviews dating back
to 1998. There is no entry on Wikipedia for the game nor Tribal Dreams. A
playthrough does exist on YouTube.

The goal of this project is to reimplement the game engine for modern
computers. Given the original data files, it should allow the game to be played
without such outdated technology as Windows 95, an optical drive, or a forced
screen resolution.

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

Gameplay is mouse driven.

The game environment was modeled in 3D and rendered into a series of images and
animations. Each location is presented as a panorama which often includes
animation. Removable objects appear superimposed at fixed locations in each
location. Movement between locations is shown with a full screen video. All
locations and transitions are loaded from the optical media. (One of three
CD-ROMs.)

The game menu appears in the same manner as one of these locations.

The spacebar opens the inventory while held. It appears at the top of the
screen, with the game paused behind it in greyscale.

Most locations include looping background audio, and most actions include an
associated audio cue. There is also an announcer at times.

The game was designed for Windows 95, but also appears to work on 64-bit
Windows 8.

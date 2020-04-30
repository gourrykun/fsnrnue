![Fate/stay night \[Réalta Nua\]](https://user-images.githubusercontent.com/217028/74502954-3ada0500-4ee7-11ea-849e-1ef29f34b512.jpg)

Fate/stay night [Réalta Nua] Ultimate Edition
=============================================

This repository [unofficially hosts GitHub-managed downloads][releases] for
*[Fate/stay night \[Réalta Nua\] Ultimate
Edition][ultimate]* – a pair of third-party 32- and 64-bit Windows installers
automating the installation, patching, and execution of the *[\[Réalta
Nua\]](https://typemoon.fandom.com/wiki/Fate/stay_night#R.C3.A9alta_Nua)*
variant of the seminal Japanese visual novel [*Fate/stay
night*](https://typemoon.fandom.com/wiki/Fate/stay_night).

## Downloads

[Current downloads hosted at this repository][releases] include:

* [Lutris-based][lutris] Linux installers: <sup>*see [installation
  instructions below](#installation)*</sup>
  * _(Recommended)_ **[One-click installer][installer-remote],** automatically
    installing *[Fate/stay night \[Réalta Nua\] Ultimate Edition][ultimate]*
    via [lutris.net browser integration](https://lutris.net/faq#url-handler).
  * **[Offline installer][installer-local],** suitable for manually
    installing *[Fate/stay night \[Réalta Nua\] Ultimate Edition][ultimate]*
    via the `lutris -i` command-line option.
* **[64-bit Windows
  installer](https://github.com/leycec/fsnrnue/releases/download/2019.03.19/fsnrnue-2019.03.19-64.zip).**
* **[32-bit Windows
  installer](https://github.com/leycec/fsnrnue/releases/download/2019.03.19/fsnrnue-2019.03.19-32.zip).**

## Installation

1. **Get _Fate/stay night [Réalta Nua]_.** Sadly, all versions of *Fate/stay
   night* (including the most recent *[Réalta Nua]* release) are unavailable
   for purchase and [thus constitute
   abandonware](https://en.wikipedia.org/wiki/Abandonware). Instead:
   1. Search for these exact terms: [`nyaa "Fate/stay night [Realta Nua] for
      Windows"`](https://www.google.com/search?q=nyaa+%22Fate%2Fstay+night+%5BRealta+Nua%5D+for+Windows%22&oq=nyaa+%22Fate%2Fstay+night+%5BRealta+Nua%5D+for+Windows%22)
   1. Click on the topmost hit. <sup>...*probably*</sup>
   1. Download the 6.4GB directory `"Fate stay night Realta Nua/"` containing
      these six files:
      * `Fate.rar`.
      * `Fate Crack.rar`.
      * `Heaven's Feel.7z`.
      * `Heaven's Feel Crack.rar`.
      * `Unlimited Blade Works.rar`.
      * `Unlimited Blade Works Crack.rar`.
1. If your current platform is:
   * **Windows:**
     1. First, follow [steps 1, 2, and 3 *only* of the "Fate/Stay Night VN
        Installation Guide
        VII."](https://www.reddit.com/r/fatestaynight/comments/7qh6ho/fatestay_night_vn_installation_guide_vii)
     1. Then follow the [official Ultimate Edition instructions][ultimate].
   * **Linux:**
     1. _(Recommended)_ **[Install *Wine
        Staging*](https://wiki.winehq.org/Wine-Staging).** See also
        instructions for:
        * [Debian-based distributions (e.g.,
          Ubuntu)](https://www.linuxuprising.com/2019/09/how-to-install-wine-staging-development.html).
     1. **[Install *Lutris*][lutris].**
     1. **Install _Fate/stay night \[Réalta Nua\] Ultimate Edition_** with
        either:
        * *(Recommended)* **[Our one-click installer][installer-remote],**
          automating installation by transparently downloading and running this
          installer under *[Lutris][lutris].*
        * **Our offline installer,** manually runnable at the command line as
          follows:
          1. [Download this file][installer-local].
          1. Open a terminal to the directory containing that file.
          1. Copy-and-paste this command into that terminal:
         
                 lutris -i fate-stay-night-realta-nua-ultimate-edition.yml

   * **macOS is currently unsupported,** as [Lutris][lutris] is currently
     Linux-specific. In theory, porting our [Lutris-specific
     installer][installer-local] to [PlayOnMac][playonmac]
     *should* be feasible but non-trivial. If someone does so, please submit an
     [issue](https://github.com/leycec/fsnrnue/issues) or [pull
     request](https://github.com/leycec/fsnrnue/pulls) and we'll update these
     instructions accordingly.

## Configuration

We strongly recommend:

* **Enabling the *Patch* → *Options* → *Skip movies in-game* option.** Consider
  watching these movies either online or via the **_Extras_** title option 
  available after successfully completing the Prologue. Attempting to play
  movies usually raises fatal exceptions (e.g., at the fade-to-white Prologue
  ending) with error messages resembling one or more of:
  * `0009:fixme:gstreamer:mpeg_splitter_sink_query_accept Unsupported subtype {e436eb84-524f-11ce-9f53-0020af0ba770}.`
  * `00:15:24 ==== An exception occured at movie.tjs(210)[(function) open], VM ip = 81 ====`
  * `00:15:25 exception: (object 0x1184E098:0x1184E098)"Cannot convert the variable type ((void) to Object)"`
* **Disabling the *Patch* → *Vita Additions* → *Play Vita OP in-game* option.**
  In addition to raising fatal exceptions, Vita movies also contain heavy
  spoilers – especially for Heaven's Feel, the final route and grand finale.
  (All remaining patches are spoiler-free.)
* **Enabling the *Display* → *Aspect Ratio* → *Standard* option** (i.e., the
  default) rather than the **_Wide_** option, which is known to be error-prone.

## Usage

Lastly, note these [undocumented keyboard
shortcuts](https://www.reddit.com/r/fatestaynight/comments/42vvy4/keyboard_shortcutshotkeys_for_fatestay_night_vn):

Key | Action
--- | ---
Space/Enter | Next line (& pause auto-read)
Down/Up Arrow | Next/Previous
A | Auto-read (toggle)
R | Review history/previous page
F | Fast skip to next scene or choice
Ctrl | Fast skip pages/scenes (hold)
S | Save menu
L | Load menu
Q | Quick Save/Load (for F1-F9)
F1-F9 | Quick load specific save data slot
Esc | Menu
Backspace | Show background (hide text)
Alt+Enter | Toggle fullscreen
C | Config

## FAQ

#### How to resolve `"Script exception raised"` errors at startup?

If you receive an error resembling `"Script exception raised Read error"` or
`"Script exception raised file://./c/program files/fate／stay night[realta nua]
ultimate edition/patch.xp3 is not XP3 archive or unsupported"` at game startup,
the Ultimate Edition installer failed to properly download one or more patches.
All such patches are locally corrupt and *must* be [manually redownloaded from
the Google Drive links given under the **Mandatory patches** section of the
original release notes for the Ultimate Edition][ultimate] into the
`fate-stay-night-realta-nua-ultimate-edition/drive_c/Program Files/Fate／stay
night[Realta Nua] Ultimate Edition/` subdirectory to which the Ultimate Edition
previously installed itself, overwriting each existing corrupt patch.

If unsure of which patches exactly require redownloading, either:

* Entirely remove the existing corrupt *Fate/stay night* installation and
  [retry from step #2 above](#installation). 
* Inspect the aforementioned subdirectory for 0-byte filenames prefixed by
  `patch_`: e.g.,

```
$ ls -l
total 4.8G
drwxr-xr-x  3 leycec leycec 4.0K Feb 14 01:23 .
drwxr-xr-x 11 leycec leycec 4.0K Feb 14 00:50 ..
drwxr-xr-x  2 leycec leycec 4.0K Feb 14 01:23 savedata
-rw-r--r--  1 leycec leycec 940M Feb 14 01:02 bgimage.xp3
-rw-r--r--  1 leycec leycec 137M Feb 14 01:03 bgm.xp3
-rw-r--r--  1 leycec leycec  200 Feb 14 01:17 config.ksc
-rw-r--r--  1 leycec leycec 4.8M Feb 14 01:03 data.xp3
-rw-r--r--  1 leycec leycec  13M Feb 14 01:03 etc.xp3
-rwxr-xr-x  1 leycec leycec 4.3M Feb 14 01:17 Fate.exe
-rw-r--r--  1 leycec leycec 300M Feb 14 01:03 fgimage.xp3
-rw-r--r--  1 leycec leycec  18M Feb 14 01:17 Flowchart.pdf
-rw-r--r--  1 leycec leycec  51M Feb 14 01:03 image.xp3
-rw-r--r--  1 leycec leycec    0 Feb 14 01:01 patch_decensor.xp3
-rw-r--r--  1 leycec leycec 1.3K Feb 14 01:32 patches.json
-rw-r--r--  1 leycec leycec 167M Feb 14 01:01 patch_h.xp3
-rw-r--r--  1 leycec leycec  15M Feb 14 00:55 patch_lang_english.xp3
-rw-r--r--  1 leycec leycec 120M Feb 14 00:55 patch.xp3
-rw-r--r--  1 leycec leycec  49K Feb 14 01:17 README-patch.html
-rw-r--r--  1 leycec leycec 8.1M Feb 14 01:03 rule.xp3
-rw-r--r--  1 leycec leycec 344M Feb 14 01:04 sound.xp3
-rw-r--r--  1 leycec leycec  23K Feb 14 01:17 supported_games.png
-rwxr-xr-x  1 leycec leycec  37M Feb 14 01:17 uninstall.exe
-rw-r--r--  1 leycec leycec  77M Feb 14 01:05 video.xp3
-rw-r--r--  1 leycec leycec 2.6G Feb 14 01:17 voice.xp3
-rw-r--r--  1 leycec leycec 1.1K Feb 14 01:17 xp3filter.tjs
```

* Run *Fate/stay night* from the command line and search for text in the
  terminal buffer resembling:

```
01:36:36 (info) Trying to read XP3 virtual file system information from : file://./c/program files/fate^stay night[realta nua] ultimate edition/patch_decensor.xp3
01:36:36 (info) Failed.
01:36:36 ==== An exception occured at initialize.tjs(197)[(function) KAGLoadScript], VM ip = 16 ====
```

In both cases, the decensor patch (i.e., `patch_decensor.xp3`) is corrupt and
should be manually redownloaded.

#### About movies

FSN has 3 routes played in that order: Fate, Unlimited Blade Works and Heavens
Feel. When a route has been completed the next one opens. The title screen
changes depending on the unlocked route. Although this is a visual novel, there
are several movies that can be played during the game or from the `Extra/Movie`
menu. The following list may not be complete:

| Movie | How to view |
| --- | --- |
| Fate opening (PS2) | complete prologue on first playthrough<br>available in Extra/movie menu from that point |
| Fate opening (PC) | available in Extra/Movie menu after completing prologue on first playthrough |
| Fate opening (PS Vita) | played at the end of day 3 on Fate route |
| UBW opening (PS2) | complete prologue when title screen shows Unlimited Blade Works<br>available in Extra/movie menu from that point |
| UBW opening (PC) | available in Extra/Movie menu after completing prologue when title screen shows UBW |
| UBW opening (PS Vita) | played at the end of day 3 on UBW route |
| HF opening (PS2) | complete prologue when title screen shows Heaven's Feel<br>available in Extra/Movie menu from that point |
| HF opening (PS Vita) | played at the end of day 3 on HF route |

Most of them can be found on streaming platforms very easily and not being able
to play them should not hinder game experience at all. To play them, it is
necessary to use the latest patches from Beast Lair (1.0.0 at the current
time). The following advices may also be of help.

Necessary settings to play movies are:

- Patch > Vita additions: all checked
- Patch > Movies: check `force movie playback using mpv`, uncheck `skip movies in-game`

Recommended settings to minimize occurences of graphical glitches are:

- Display > Window
- Display > Aspect ratio: standard

Since another program (mpv) is used to play movies, the following
recommendations may also be of use:

Playing with fullscreen may lead to graphical glitches in game once video
stops. Or not, your mileage may vary. Pressing `ALT TAB` may be necessary to
bring mpv player on foreground whether in windowed or fullscreen mode.

Using `CTRL` to fast forward to start of movie may lead to in game sounds to
keep playing while the movie is playing. It is best to use `CTRL` with care and
proceed slowly till movie starts.

Lastly, when browsing movies in the `Extra/Movie` menu, one may encounter an
error dialog box showing `cannot convert the variable type ((void) to Object)`.
It happens when using mouse to browse to the right (either clicking on the
scroll bar or using the mouse wheel). Using the left/right arrows of the
keyboard allows to select unseen thumbnails without crashing the game.

## Authors

Authoritative credit for the Ultimate Edition and bundled patches goes entirely
to the [Beast's Lair fandom](http://forums.nrvnqsr.com) – notably:

* Project leads:
  * **Jacktheinfinite101.**
  * **Quibi.**
  * **Kotonoha.**
* The Cast:
  * **Jacktheinfinite101:** Lead editor, programming, some image editing.
  * **Quibi:** Lead programmer, installer creation.
  * **Koto:** Lead translator, text editing, some image editing.
  * **Hintay:** Additional programming.
  * **Anonamous:** Additional programming.
  * **uyjulian:** Krkrz development.
  * **Waku Waku:** Lead image editor, programming consultant, PS2 resources,
    legacy project.
  * **ニサンカタンソ:** Additional programming.
  * **NM64:** Audio editing, beta testing, media assets.
  * **SmilingWolf:** Upscaled image assets.
  * **Hyarion:** Initial translation of Fate H alts.
  * **MeruP:** Programming.
  * **Terrafire:** Script comparisons.
  * **Dallas Hickan:** Additional image editing.
  * **GameCreater32:** Custom voice replay icons, supplemental tools.
  * **Commander Rase:** Beta Testing.
  * **Thryfe:** Beta Testing.
  * **Inuhanyou:** Beta Testing.
  * **SkitZoFrenic:** Beta Testing.
  * **Ownsin:** Beta Testing.
  * **UnlimitedBladeWorks:** Beta Testing.
  * **Taka-jun, ArchDemon, Tjm, and puKKa from Mirror Moon:** Original
    translation.
  * **bishopcruz and Annonymous:** First H uncensor patch.
  * **Himeros and Belldandy100:** Second H uncensor patch.
  * **[/u/dumbyoyo](https://www.reddit.com/user/dumbyoyo):** Keyboard
    shortcuts.
  * Special thanks to [any other BL members](http://forums.nrvnqsr.com) who
    helped out.

This Linux support's for you, stalwart Nasuverse heroes.


[lutris]:    https://lutris.net
[playonmac]: https://www.playonmac.com
[releases]:  https://github.com/leycec/fsnrnue/releases
[ultimate]:  https://forums.nrvnqsr.com/showthread.php/8229
[installer-local]: /lutris/fate-stay-night-realta-nua-ultimate-edition.yml
[installer-remote]: https://leycec.github.io/fsnrnue/lutris/installer_redirect.html

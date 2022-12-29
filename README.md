# Multimedia Programming with Pure Data
Pure Data code from the book [_Multimedia Programming with Pure Data_](https://www.amazon.com/Multimedia-Programming-Pure-Bryan-Chung/dp/1782164642) by Bryan WC Chung. The book is very good!

## Installing Pure Data

The book was written targeting Pd-extended. However, Pd-extended is no longer maintained and is deprecated. It has fallen behind Pd Vanilla. Since Pd-extended was Pd Vanilla plus some libraries, all we need to do is install Pd Vanilla and then the needed libraries. So please don't worry about the reviews that state the library the book uses is out of data, since the required libraries that are used in the book can easily be installed into Pd Vanilla.

### Libraries

The required libraries (also known as externals) to get through the book's code are:

* `Gem`: This is for the graphics objects.
* `cyclone`: This is for the `counter` object used first in Chapter 1.

Note: capitalization matters when installing.

### Installing a library

The following runs through installing Pure Data and the Gem library. Follow the same procedure for the `cyclone` library as for the `Gem` library described below.

1. [Install Pd Vanilla](https://puredata.info/)
2. After installation, open Pure Data
3. Select **Help** -> **Find Externals**
4. Search for "gem"
5. Select the Gem library with the most recent release date (0.94 at time of writing) and click **Install**
6. Select **Yes** if or when asked to install Gem to your `Pd/externals` directory (you may not be asked this).
    * If you run Pure Data directory after running the installer, it's possible that Pure Data has not created a patches and externals directory. In this case and on my machine, the default directory for the prompt `Install externals to directory` is `C:\Program Files\Pd\bin`. (I installed Pure Data via the Windows installer.) The setup described here failed when I chose this path.
    * However, when starting up Pure Data outside of luanching initially from the installer, Pure Data should ask you to create a directory when starting up for saving patches and externals. If happens, click yes, and then the default directory for externals is `C:\Users\<username>\Documents\Pd\externals`.
7. Wait until the progress bar becomes full
    * You should see a message `[deken] Successfully installed 'Gem'!` in the main Pd window's console
9. Close the **Find externals** window
10. Select **File** -> **Preferences** -> **Startup...**
11. Select **New...** and enter in `Gem`. Please note that the case is important. Select **Ok**.
12. Select **Ok** again to exit out of the **Pd libraries to load on startup window**
13. Restart Pure Data
14. Something like the following should be in your console window:
    
    ```
    GEM: Graphics Environment for Multimedia
    GEM: ver: 0.94.git v0.94
    GEM: compiled  on Feb 12 2019
    GEM: maintained by IOhannes m zmoelnig
    GEM: Authors :	Mark Danks (original version)
    GEM:		Chris Clepper
    GEM:		Cyrille Henry
    GEM:		IOhannes m zmoelnig
    GEM: with help by Guenter Geiger, Daniel Heckenberg, James Tittle, Hans-Christoph Steiner, et al.
    GEM: found a bug? miss a feature? please report it:
    GEM: 	homepage https://gem.iem.at/
    GEM: 	bug-tracker https://bugs.gem.iem.at/
    GEM: 	mailing-list https://lists.puredata.info/listinfo/gem-dev/
    GEM: compiled for MMX/SSE2 architecture
    GEM: using SSE2 optimization
    GEM: detected 16 CPUs
    GEM: image loading plugins: magick SGI STB jpeg tiff
    GEM: film loading plugins: DirectShow
    GEM: image saving plugins: SGI STB jpeg magick tiff
    GEM: model loading plugins: ASSIMP3 OBJ
    GEM: video capture plugins: VIDS decklink vnc
    ```

Once you have installed the `cyclone` library and added it to startup (be sure to add it as all lowercase), then you should additionally see the following printed out at startup:

```
--------------------------------------------------------------------
:: Cyclone 0.6-1; Released june 8th 2022
:: License: BSD-3-Clause (aka Revised BSD License)
:: Copyright © 2003-2021 - Krzysztof Czaja, Hans-Christoph Steiner,
:: Fred Jan Kraan, Alexandre Porres, Derek Kwan, Matt Barber
:: and others.
:: -----------------------------------------------------------------
:: Cyclone 0.6-1 needs at least Pd 0.52-0
             (you have 0.53-0, you're good!)
:: Loading the cyclone library did the following:
::   - A) Loaded the non alphanumeric objects, which are:
:: [!-], [!-~], [!/], [!/~], [!=~], [%~], [+=~], [<=~], [<~],
:: [==~], [>=~] and [>~]
::   - B) Added C:/Users/bmitc/Documents/Pd/externals/cyclone
:: to Pd's path so the other objects can be loaded too
:: but use [declare -path cyclone] to guarantee search priority
:: in the patch
--------------------------------------------------------------------
```

Here's a screenshot of my startup configuration:

![image](https://user-images.githubusercontent.com/65685447/209909925-debed46f-42b8-42b3-a1f9-967417428196.png)

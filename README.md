# Multimedia Programming with Pure Data
Pure Data code from the book [_Multimedia Programming with Pure Data_](https://www.amazon.com/Multimedia-Programming-Pure-Bryan-Chung/dp/1782164642) by Bryan WC Chung. The book is very good!

## Installing Pure Data

The book was written targeting Pd-extended. However, Pd-extended is no longer maintained and is deprecated. It has fallen behind Pd Vanilla. Since Pd-extended was Pd Vanilla plus some libraries, all we need to do is install Pd Vanilla and then the Gem library. So please don't worry about the reviews that state the library the book uses is out of data, since it can easily be installed into Pd Vanilla.

1. [Install Pd Vanilla](https://puredata.info/)
2. After installation, open Pure Data
3. Select **Help** -> **Find Externals**
4. Search for "gem"
5. Select the Gem library with the most recent release date.
6. Select **Yes** when asked to install Gem to your `Pd/externals` directory
7. Wait until the progress bar becomes full
8. Close the **Find externals** window
9. Select **File** -> **Preferences** -> **Startup...**
10. Select **New...** and enter in `Gem`. Please note that the case is important. Select **Ok**.
11. Select **Ok** again to exit out of the **Pd libraries to load on startup window**
12. Restart Pure Data
13. Something like the following should be in your console window:
    
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

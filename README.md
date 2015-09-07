# LaTeX Homework Styles

Custom LaTeX files created for my homework assignments at Harvey Mudd College.

Mostly these are metapackages, with some settings and some simple macros. I've been building up this set of customizations since I started using LaTeX for my homework at the beginning of 2012.

## Chit Chat

### There's a Bug!

Those with a GitHub account can open an issue using the issue tracker.

Those at Mudd can shoot me an email, and I'll do my best to fix the problem promptly.

### I Don't Like Your Style

Typographic critique or advice is appreciated. Flaming is not.

Please remember: I'm just providing this repository publicly because I have it for my homework anyway. It's great if this is useful to others, but it's not my job to meet everyone's needs.## Making it Work

## Making it Work

### Prerequisites

In order to compile LaTeX documents from source with this set of styles, the following are required:
* Make sure you have the desired .tex file.
* Make sure this repository (or at least the common_files subdirectory) can be seen by TeX. There are two options for this:
  * Place this repository in your local texmf tree (and make sure LaTeX knows about it).
    * This solution is a better practice, as it allows the styles to be used in any LaTeX files without duplicating them all over.
      * This is my current solution.
      * This is especially convenient if the style files are changed periodically, as in the case of this repository, because only one copy must be changed.
    * Unfortunately the location of this directory and the process for telling LaTeX about it vary by installation, so I can't provide directions for everybody. Fortunately this is a common issue, so just search online ("local texmf tree" and whatnot) for directions. For reference:
      * On my Ubuntu system with a custom-managed LaTeX installation, I currently have this repository at ~/texmf/tex/latex/Homework-Styles.
  * Place this repository in the same directory as the .tex file being compiled. 
    * This solution seems simpler at first, but it requires the files to be copied anywhere they need to be used.
      * This is what I used to do.
      * This can be rather inconvenient for this sort of repository, which changes periodically yet may be used for homework in multiple course.
* Install the required fonts. By default I use free and open source fonts, and the current choices aren't installed by default on most systems. I've chosen good fonts, and installing them is very simple, so I would highly recommend doing so.
  * To use my chosen fonts: just download them, unzip, and install. Many file browsers (e.g. Windows Explorer and Nautilus) provide a button to install font files directly from the file browser.
    * TeX Gyre Heros: http://www.gust.org.pl/projects/e-foundry/tex-gyre/heros
      * Direct Download: http://www.gust.org.pl/projects/e-foundry/tex-gyre/heros/qhv2.004otf.zip
    * TeX Gyre Pagella: http://www.gust.org.pl/projects/e-foundry/tex-gyre/pagella
      * Direct Download: http://www.gust.org.pl/projects/e-foundry/tex-gyre/pagella/qpl2.004otf.zip
    * TeX Gyre Pagella Math: http://www.gust.org.pl/projects/e-foundry/tg-math/download
      * Direct Download: http://www.gust.org.pl/projects/e-foundry/tg-math/download/texgyreschola-math-1533.zip
    * Inconsolata: http://www.google.com/fonts/specimen/Inconsolata
      * Direct Download: http://www.google.com/fonts/download?kit=CNj0Ze1H6w4FVgc32wmZS4fD-WQWLbF4rYwcBGowFYY
  * To use different fonts: change or comment-out the \set...font{<>} lines in hw_type.sty. I offer no guarantees as to typesetting quality, nor even compilation errors. Your mileage may vary.

Once those files are in place, compile the desired LaTeX documents. Note:
* Make sure your LaTeX installation is up-to-date! I use some recent features of actively-developed packages, and your LaTeX installation may have versions that are a few years old. (This is the most common problem I've encountered with my styles.)
* Most major LaTeX distributions will automatically fetch new third-party packages used from CTAN.
  * If your system does not do this, you may have to manually install packages requested during compilation.
  * On my Windows system, MikTeX automatically installs new packages during compilation.
  * On my Linux system, I have switched to a custom-managed LaTeX installation in order to have more control over installed packaged. However when packages are not found during compilation, I do have to manually run tlmgr manually in order to install them.
* Use XeLaTeX. These documents are written for the XeLaTeX engine, which is included in every LaTeX installations I've encountered. All one needs to do is to make it the default engine. Existing files written for pdfTeX should still compile just fine.

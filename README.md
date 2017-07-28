# Magnify

## A magnifier to investigate raw and deconvoluted waveforms.

### Usage

Magnify can be run with a helper script kept in the source directory:

```
/path/to/magnify/magnify.sh /path/to/file.root [frame]
```

The `frame` names the type of output of the signal processing to display.
WC prototype produces a single `decon`.
WC toolkit produces either `wiener` or `gauss`.

The `magnify.sh` shell script wraps up the main ROOT scripts to load the code and then run it.  
They can be run manually like:

```
cd scripts/
root -l loadClasses.C 'Magnify.C("path/to/rootfile")'
# or
root -l loadClasses.C 'Magnify.C("path/to/rootfile","gauss")'
```

An (old prototype) example ROOT file of waveforms can be found at http://www.phy.bnl.gov/xqian/talks/wire-cell/2D_display_3455_0_0.root

If one omits the file name, a dialog will open to let user select the file:
```
cd scripts/
root -l loadClasses.C Magnify.C
```

### Screenshot

![screenshot](data/screenshot.png?raw=true "Screenshot")

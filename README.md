MicrOMEGAs Environment
========================
This package provides an environment that allows one to install and use
[MicrOMEGAs](http://lapth.cnrs.fr/micromegas/)

Installation
------------
- Make sure that flatpak and flatpak-builder are installed
- Install the software development kit
```
flatpak install flathub org.freedesktop.Platform//20.08 org.freedesktop.Sdk//20.08
```
- Compile and install MicrOMEGAs environment
```
flatpak-builder build-dir fr.cnrs.lapth.MicrOMEGAs.yaml --force-clean --install --user --jobs=4
```

Usage
-----
- Show the help (includes more commands than this README)
```
flatpak run fr.cnrs.lapth.MicrOMEGAs
flatpak run fr.cnrs.lapth.MicrOMEGAs -?
```
- Install MicrOMEGAs 5.2.4 (the flatpak contains the source code)
```
alias mo='flatpak run fr.cnrs.lapth.MicrOMEGAs'
mo install
```
- Use as usual (just prefix the commands with `flatpak run
  fr.cnrs.lapth.MicrOMEGAs` or use the alias mo)
```
alias mo='flatpak run fr.cnrs.lapth.MicrOMEGAs'
cd micromegas_5.2.4
mo ./newProject my_project
cd my_project
mo make
cd work
mo ./calchep
```

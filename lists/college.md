# College Packages

## Official

### install fortran

gcc-fortran arpack
mpdecimal gnuplot

### install python modules

python-gnuplot python-tqdm
python-numpy python-pandas
python-pytables python-scipy
python-pyarrow python-openpyxl
python-tabulate python-matplotlib

### install texlive

texlive texlive-langenglish
texstudio minted biber pdftk
dblatex latex2html latex2rtf

### install opencv library

python-opencv vtk hdf5-openmpi

--------------------------------------------------------------------------------

## AUR

### install ms fonts

- https://aur.archlinux.org/packages/ttf-tahoma/
- https://aur.archlinux.org/packages/ttf-ms-fonts/
- https://aur.archlinux.org/packages/ttf-vista-fonts/

### install python additionals

- https://aur.archlinux.org/packages/python-soundfile/
- https://aur.archlinux.org/packages/python-pyfftw/

### install shell additional

- https://aur.archlinux.org/packages/ttyplot-git/
- https://aur.archlinux.org/packages/ncurses5-compat-libs/

### wps office

- https://aur.archlinux.org/packages/libtiff5/
- https://aur.archlinux.org/packages/wps-office/
- https://aur.archlinux.org/packages/ttf-wps-fonts/

--------------------------------------------------------------------------------

## Configurations

### configure texstudio

```sh
"latex -shell-escape -src -interaction=nonstopmode %.tex"
"pdflatex -shell-escape -synctex=1 -interaction=nonstopmode %.tex"
```

```sh
FancyVerb error \end{minted}
Just delete \t (Tab) after \end{minted}
```

```sh
Uncheck 'Adv. Editor'->'Structure Panel'->'Mark structure elements beyond \end{document}'
```

### configure wps office

```sh
sudo rm -f /usr/share/applications/wps-office-pdf.desktop
sudo rm -f /usr/share/applications/wps-office-prometheus.desktop
sudo sed -i '/^$/d' /usr/share/desktop-directories/wps-office.directory
echo 'NoDisplay=true' | sudo tee -a /usr/share/desktop-directories/wps-office.directory
```

# dhutchis-cv
Dylan Hutchison Curriculum Vit&#230;

[**View the latest PDF here**](https://github.com/dhutchis/dhutchis-cv/raw/master/dhutchis-cv.pdf).

To compile a subset of pages:

```
pdftk A=dhutchis-cv.pdf cat A1-3 output dhutchis-cv-3.pdf

# Replace pdf metadata that pdftk butchers
pdftk dhutchis-cv.pdf dump_data output orig.txt
emacs orig.txt # Edit metadata, setting NumberOfPages to 3 and removing lost hyperlinks

pdftk dhutchis-cv-3.pdf update_info new.txt output dhutchis-cv-3-new.pdf
mv dhutchis-cv-3-new.pdf dhutchis-cv-3.pdf
```

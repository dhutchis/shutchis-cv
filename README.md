# shutchis-cv
Shana Hutchison Curriculum Vit&#230;

[**View the latest PDF here**](https://github.com/dhutchis/shutchis-cv/raw/master/shutchis-cv.pdf).

To compile a subset of pages:

```
pdftk A=shutchis-cv.pdf cat A1-3 output shutchis-cv-3.pdf

# Replace pdf metadata that pdftk butchers
pdftk shutchis-cv.pdf dump_data output orig.txt
emacs orig.txt # Edit metadata, setting NumberOfPages to 3 and removing lost hyperlinks

pdftk shutchis-cv-3.pdf update_info new.txt output shutchis-cv-3-new.pdf
mv shutchis-cv-3-new.pdf shutchis-cv-3.pdf
```

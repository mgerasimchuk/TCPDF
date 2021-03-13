# TCPDF with custom fonts injected

Original README: [README-ORIGINAL.md](README-ORIGINAL.md)

# How to add new font

```
Go to https://fonts.google.com/specimen/Open+Sans
```

```
wget -O fonts-original/open-sans.zip 'https://fonts.google.com/download?family=Open%20Sans'
```

```
mkdir fonts-original/open-sans ;\
unzip -d fonts-original/open-sans fonts-original/open-sans.zip ;\
rm fonts-original/open-sans.zip
```

```
tools/tcpdf_addfont.php --fonts $(find fonts-original/open-sans/*.ttf | paste -sd "," -) --outpath fonts
```

```
git add . ; git commit -m "add open-sans" ; git push origin custom-fonts
```
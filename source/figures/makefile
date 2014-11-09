
# Atumacao para converter imagens
# by Leandro Sehnem Heck

# Lista os arquivos SVG
svg_images := $(wildcard *.svg)
png_images := $(svg_images:.svg=.png)

# Converte para PDF somente os SVGs modificados
all: $(png_images)

# Converte de SVG para PNG
%.png: %.svg
	@ echo "# Gerando: $(@)"
	@ #inkscape --export-pdf=$(@D)/$(basename $(@F)).pdf --export-ignore-filters --export-text-to-path $(@D)/$(basename $(@F)).svg
	@ inkscape --export-dpi=300 --export-background-opacity=0 -f $^ -e $@

# Remove arquivos temporarios
clean:
	@ rm -f *~

# Remove os png
superclean:
	@ rm -f $(png_images)
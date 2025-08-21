# MinecraftScad
Repo for the script to build a name with Minecraft Style using OpenScad and Python to convert .svg in .scad
# To convert .svg in .scad
    # One way
        New-Item -ItemType Directory -Force glyphs
        >> Get-ChildItem -Path .\letters_svg\ -Filter *.svg | ForEach-Object {
        >>   py .\converter.py $_.FullName -d .\glyphs
        >> }
    # Another
        python converter.py letters_svg/A.svg   


# To use glyphs
    Delete scale factor from module glyphs and we have to rename glyphs (example glyph_A ...)
    Collocate glyphs in .scad to use the modules

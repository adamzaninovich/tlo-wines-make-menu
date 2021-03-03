# tlo-wines-make-menu

This script compiles a pdf menu for Tlo Wines from individual pages.
It will order the pages as specified by their naming (see example below).
It will also clear our any unnecessary tags and data from the final PDF.

Before using, you will need to add a `secrets.sh` file in the same directory as the script. This file should export the following variables:
- `TLOVID_BUCKET_URL`: The url to the GCP bucket page
- `TLOVID_LBCACHE_URL`: The url to the GCP load balancer caching page


To use, name the pages starting with the page number like this:

    1 Tlo QR By the glass Menu-March.pdf
    1.1 QR Menu Wine Club Week.pdf
    2 Tlo QR Bottle Menu (Rosé_Whites).pdf
    3 Tlo QR Bottle Menu (light reds).pdf
    4 Tlo QR Bottle Menu (heavy reds).pdf
    5 Tlo QR Bottle Menu (red blends_dessert).pdf
    7 Tlo QR Menu Merch.pdf

Then, simply run `make_menu` in that directory and answer the prompts

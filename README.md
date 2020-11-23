# Script Snippets
A collection of small (mostly one liner) script snippets (Linux, POSIX-shell) which I find useful.

### Search and replace a text on many files
``grep -RIl 'text' | xargs sed -i 's/text/replace/g'``

### Get volume using amixer
``amixer -M get Master | awk -- '/^  M/ { print $4 }' | tr -d []``

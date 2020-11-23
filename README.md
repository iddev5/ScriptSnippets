# Script Snippets
A collection of small (mostly one liner) script snippets (Linux, POSIX-shell, Fish-shell) which I find useful.

### Search and replace a text on many files
```sh 
grep -RIl 'text' | xargs sed -i 's/text/replace/g'
```

### Get volume using amixer
```sh 
amixer -M get Master | awk -- '/^ {2}M/ { print $4 }' | tr -d []
```

# License
This software is licensed under the terms of MIT License (See [LICENSE](LICENSE)).  
Copyright 2020 Ayush Bardhan Tripathy.

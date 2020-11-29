# Script Snippets
A collection of small (mostly one liner) script snippets (Linux, POSIX-shell, Fish-shell) which I find useful.

### Search and replace a text on many files
```sh 
grep -RIl 'text' | xargs sed -i 's/text/replace/g'
```

### Get volume using amixer
```sh 
amixer -M get Master | awk -- '/Mono:/ { print $4 }' | tr -d []
```

### Get battery percentage and status
```sh
# Percentage
upower -i /org/freedesktop/UPower/devices/battery_BAT0 | awk -- '/percentage/ { print $2 }'

# Status
upower -i /org/freedesktop/UPower/devices/battery_BAT0 | awk -- '/state/ { print $2 }' | tr '-' ' '
```

# License
This project is licensed under the terms of MIT No Attribution License (See [LICENSE](LICENSE)).  
Copyright 2020 Ayush Bardhan Tripathy.

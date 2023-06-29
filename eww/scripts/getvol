#!/bin/sh

# Get the index of the selected sink:
getsink() {
    pacmd list-sinks |
        awk '/index:/{i++} /* index:/{print i; exit}'
}

# Get the selected sink volume
getvolume() {
    pacmd list-sinks |
        awk '/^\svolume:/{i++} i=='$(getsink)'{print $5; exit}'
}

getvolume

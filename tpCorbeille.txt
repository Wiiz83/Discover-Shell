#!/bin/bash
i = 0
for f in $@
do
    if [$i = 0]
    then
        i =1
        
    elif [$1 = efface]
    then
        mv $f $HOME/.corbeille/
        
    elif [$1 = restaure]
    then
        mv ~/.corbeille/$f $f
        
    elif [$1 = info]
    then
        echo info
        
    elif [$1 = vide]
    then
        rm $HOME/.corbeille/*
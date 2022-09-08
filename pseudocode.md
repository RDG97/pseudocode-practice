# Changing the oil in a car

## About and assumptions
1. car is parked on a flat surface with the hood up.

2. car needs an oil change (due to mileage)

3. We have the appropriate tools (ratchet with socket, oil pan,)

4. We have the appropriate type and amount of new oil, and oil filter.

## Initialize variables

1. newOil
    * Fresh oil we will be replacing the old stuff with
    
        -addOil
        
        -oilAdded (true/false)

2. oldOil

    * The oil thats being replaced... its been how long?
    
        -oldDrained (true/false)

3. dripPan

    * Catches the old oil when its time for it to come out
    
        -dripPanLocation

4. fillPort
    * Where we will be putting the putting in the new oil
    
        -removePort
        
        -replacePort
        
5. drainPlug

    * What we remove to get the old oil out
    
        -drainPlugLocation
        
        -removeplug
        
        -replacePlug
        
6. dipStick

    * How we check oil levels
    
        -oilLVL (low, high, good)
        
7. oilFilter

    * this needs to be replaced also
    
        -replaceFilter
        
## Functions

```
FUNCTION removeOld:
    * let dripPanLocation = on ground directly underneath drainPlugLocation
    * IF dripPanLocation = undear drainPlugLocation
            THEN removePlug
    * IF oldOil = still dripping
        THEN wait 5 minuets and check again
        IF ELSE replacePlug replaceFilter return dripPanLocation to original state
    *let oldDrained = true
        END

FUNCTION addNew:
    IF oldDrained = true
        Then removePort
        then addOil
        then replacePort
        IF ELSE run removeOld
    LET oilAdded = true
        END

FUNCTION checkOil
    if oiladded = true
        then removeStick
        IF ELSE run addNew
    If oilLVL = good 
        then replaceStick
        if else go back to autozone :(
    END
```
## Running the program
```
removeOld
addNew
checkOil
    END
```




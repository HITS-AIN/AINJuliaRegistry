# AINJuliaRegistry

Registry for simplifying the installation of Julia packages produced by AIN group.

Packages registered with the general registry of Julia will not be registered here too.


## Using the registry

To use this registry, enter package mode with ```]``` in the REPL and execute (you may prompted for your github credentials):

```
registry add https://github.com/HITS-AIN/AINJuliaRegistry
```

If used with a fresh installation of Julia, use before (see issue [here](https://forum.mimiframework.org/t/error-installing-mimi-under-v1-3-1/109/4)):

```
registry add https://github.com/JuliaRegistries/General
```

## Updating packages in AINJuliaRegistry

Switch into "package mode" with ```]``` and add type ```registry update AINJuliaRegistry```.

(You may prompted for your github credentials.)

This will make Julia update all packages associated with AINJuliaRegistry registry.

Alternatively, enter package mode and type ```up```. This will update all installed Julia packages, including the ones of this registry.

## Removing the registry

To remove this registry simply use:

```
registry rm AINJuliaRegistry
```

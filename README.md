# AINJuliaRegistry

Registry for simplifying the installation of Julia packages produced by AIN group.

Packages registered with the general registry of Julia will not be registered here too.


## Using the registry

To use this registry, enter package mode with ```]``` and execute (you may prompted for your github credentials):

```
registry add https://github.com/HITS-AIN/AINJuliaRegistry
```

If used with a fresh installation of Julia, use before (see issue [here](https://forum.mimiframework.org/t/error-installing-mimi-under-v1-3-1/109/4)):

```
registry add https://github.com/HITS-AIN/AINJuliaRegistry
```

## Removing the registry

To remove this registry simply use:

```
registry rm AINJuliaRegistry
```

<h1 align="center">AINJuliaRegistry</h1>

<p align="center">
  <img width="200" height="200" src=ain_logo_no_shadow.jpg>
</p>

##  ℹ What is this?

A registry for simplifying the installation of Julia packages produced by the [AIN group](https://www.h-its.org/research/ain/).

Packages registered with the general registry of Julia will not be registered here too.

Software developed by the AIN can be found [here](https://github.com/HITS-AIN).

## <img width="27" height="17.5" src=smalljulia.png> Installing Julia

The easiest way of installing Julia is by downloading a binary file and simply uncompressing it in your folder of choice. Please see [here](https://julialang.org/downloads/) for platform specific instructions. Alternatively, one may choose to compile Julia from the source code.

## 🚴 Using the registry

To use this registry, enter package mode with ```]``` while in the Julia REPL and execute:

```
registry add https://github.com/HITS-AIN/AINJuliaRegistry
```

If used with a fresh installation of Julia, you may need to use the following line (see issue [here](https://forum.mimiframework.org/t/error-installing-mimi-under-v1-3-1/109/4)):

```
registry add https://github.com/JuliaRegistries/General
```

## ⇮ Updating packages in AINJuliaRegistry

Switch into "package mode" with ```]``` and add type ```registry update AINJuliaRegistry```.

This will make Julia update all packages associated with AINJuliaRegistry registry.

Alternatively, enter package mode and type ```up```. This will update all installed Julia packages, including the ones of this registry.

## 🗑 Removing the registry

To remove this registry simply use:

```
registry rm AINJuliaRegistry
```
This will affect only your own system without any consequences for this registry or other users.


## 🛠 Notes for HITS-AIN maintainers

### Registering Julia packages

To register a package to this registry, it is recommended to use [LocalRegistry.jl](https://github.com/GunnarFarneback/LocalRegistry.jl).
Below is an example of the actual registration.
Note that you will first need to add the registry "AINJuliaRegistry" to your system (see above how) before you can register your own package with it.
The function `register` takes as the first argument the location of the package and as a second argument the name of the registry we  want to register our package with. 
```
using LocalRegistry
register("/home/nikos/.julia/dev/SDSS_RM_Resampler/",registry="AINJuliaRegistry")
```

### Remove package from registry 

Currently, this has to be done manually. 
Simply delete the directory in the present repository that holds the relevant contents.
Also carefully remove the corresponding line from file `Registry.toml`.

❗Accidentally removing the wrong folder or line will cause problems to the registry for all users.

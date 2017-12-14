# NuWro Singularity recipes

This repository contains Singularity recipes for containers with [NuWro](https://github.com/NuWro/nuwro) releases (starting from 17.09).

The builds can be found in [Singularity Hub](https://singularity-hub.org/collections/265).

For more information about Singularity please visit [Singularity Used Guide](http://singularity.lbl.gov/user-guide).

---

* To download an image from Singularity Hub use `pull`:

```
$ singularity pull shub://NuWro/builds:[tag]
```

where `tag = YY.MM` (please make sure capitalization is correct - it is case sensitive), e.g. 

```
$ singularity pull shub://NuWro/builds:17.09
```

* Downloaded image (by default) has the following name:

```
[user]-[repo]-[branch]-[tag].simg
```

e.g., 

```
NuWro-builds-master-17.09.simg
```

* Information about software versions installed in a container is stores in its metadata. To check it use `inspect`, e.g.

```
$ singularity inspect NuWro-builds-master-17.09.simg 
{
    "MAINTAINER": "tomasz.golan@gmail.com",
    "NUWRO": "17.09",
    "ROOT": "5.34/36",
    "OS": "Ubuntu14.04",
    ...
}

```

* Any application can be executed from a container using `exec`, e.g.

```
$ singularity exec NuWro-builds-master-17.09.simg nuwro
```

or

```
$ singularity exec NuWro-builds-master-17.09.simg myroot 
```

* NuWro containers are set up to run NuWro, by default:

```
singularity run [img file]
```

or 

```
./[img file]
```

are equivalent to `singularity exec [img file] nuwro`, e.g.

```
./NuWro-builds-master-17.09.simg -p "beam_energy = 1234"
```

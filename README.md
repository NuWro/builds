# NuWro Singularity recipes

* [Singularity Hub](https://singularity-hub.org/collections/265)

* downloading an image

```
singularity pull shub://NuWro/builds:[tag]
```

e.g. `singularity pull shub://NuWro/builds:1709`

* using an image

```
singularity run [img file]
```

or `./[img file]`

* checking labels

```
singularity inspect [img file]
```

* [more info](http://singularity.lbl.gov/user-guide)
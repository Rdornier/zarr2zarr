zarr2zarr
=====
This tool converts back and forth OME-zarr files from 
[zarr-v2](https://zarr-specs.readthedocs.io/en/latest/v2/v2.0.html) 
to [zarr-v3](https://zarr-specs.readthedocs.io/en/latest/v3/core/v3.0.html).
standard.


## Installation
### zarr2zarr
1. Clone the repository
```dtd
git clone https://github.com/glencoesoftware/zarr2zarr.git
```

2. Build the app and skip the tests
```dtd
gradle build -x test
```

3. Extract the content of the zip (or tar) file 
``` dtd
/build/distributions/zarr2zarr-VERSION.zip`
```

### blosc
This application needs [blosc](https://github.com/Blosc/c-blosc) to run properly. If you don't have it installed, 
you can [install it or download the pre-built dll](https://github.com/glencoesoftware/bioformats2raw?tab=readme-ov-file#requirements).

## Usage

- Open a terminal under the bin folder
````dtd
/build/distributions/zarr2zarr-VERSION/bin
````

- Write down the following command to convert a **zarr-v2 file to a zarr-v3 file**
```dtd
$ /zarr2zarr v2.zarr v3.zarr
```
where `v2.zarr` and `v3.zarr` are absolute path.

- Write down the following command to convert a **zarr-v3 file to a zarr-v2 file**
```dtd
$ /zarr2zarr v3.zarr v2-output.zarr --write-v2
```
where `v2-output.zarr` and `v3.zarr` are absolute path.

- Several parameters can be added as arguments (chunk, shard...). You can have a look to them by calling the help
```dtd
$ /zarr2zarr --help
```


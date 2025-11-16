# HDF5AnnData

Implementation of an HDF5-backed `AnnData` object. This class provides
an interface to a H5AD file and minimal data is stored in memory until
it is requested by the user. It is primarily designed as an intermediate
object when reading/writing H5AD files but can be useful for accessing
parts of large files.

See
[AnnData-usage](https://anndataR.data-intuitive.com/reference/AnnData-usage.md)
for details on creating and using `AnnData` objects.

## Value

An `HDF5AnnData` object

## See also

[AnnData-usage](https://anndataR.data-intuitive.com/reference/AnnData-usage.md)
for details on creating and using `AnnData` objects

Other AnnData classes:
[`AbstractAnnData`](https://anndataR.data-intuitive.com/reference/AbstractAnnData.md),
[`AnnDataView`](https://anndataR.data-intuitive.com/reference/AnnDataView.md),
[`InMemoryAnnData`](https://anndataR.data-intuitive.com/reference/InMemoryAnnData.md),
[`ReticulateAnnData`](https://anndataR.data-intuitive.com/reference/ReticulateAnnData.md)

## Super class

[`anndataR::AbstractAnnData`](https://anndataR.data-intuitive.com/reference/AbstractAnnData.md)
-\> `HDF5AnnData`

## Active bindings

- `X`:

  See
  [AnnData-usage](https://anndataR.data-intuitive.com/reference/AnnData-usage.md)

- `layers`:

  See
  [AnnData-usage](https://anndataR.data-intuitive.com/reference/AnnData-usage.md)

- `obsm`:

  See
  [AnnData-usage](https://anndataR.data-intuitive.com/reference/AnnData-usage.md)

- `varm`:

  See
  [AnnData-usage](https://anndataR.data-intuitive.com/reference/AnnData-usage.md)

- `obsp`:

  See
  [AnnData-usage](https://anndataR.data-intuitive.com/reference/AnnData-usage.md)

- `varp`:

  See
  [AnnData-usage](https://anndataR.data-intuitive.com/reference/AnnData-usage.md)

- `obs`:

  See
  [AnnData-usage](https://anndataR.data-intuitive.com/reference/AnnData-usage.md)

- `var`:

  See
  [AnnData-usage](https://anndataR.data-intuitive.com/reference/AnnData-usage.md)

- `obs_names`:

  See
  [AnnData-usage](https://anndataR.data-intuitive.com/reference/AnnData-usage.md)

- `var_names`:

  See
  [AnnData-usage](https://anndataR.data-intuitive.com/reference/AnnData-usage.md)

- `uns`:

  See
  [AnnData-usage](https://anndataR.data-intuitive.com/reference/AnnData-usage.md)

## Methods

### Public methods

- [`HDF5AnnData$new()`](#method-HDF5AnnData-new)

- [`HDF5AnnData$close()`](#method-HDF5AnnData-close)

- [`HDF5AnnData$n_obs()`](#method-HDF5AnnData-n_obs)

- [`HDF5AnnData$n_vars()`](#method-HDF5AnnData-n_vars)

Inherited methods

- [`anndataR::AbstractAnnData$as_HDF5AnnData()`](https://anndataR.data-intuitive.com/reference/AbstractAnnData.html#method-as_HDF5AnnData)
- [`anndataR::AbstractAnnData$as_InMemoryAnnData()`](https://anndataR.data-intuitive.com/reference/AbstractAnnData.html#method-as_InMemoryAnnData)
- [`anndataR::AbstractAnnData$as_ReticulateAnnData()`](https://anndataR.data-intuitive.com/reference/AbstractAnnData.html#method-as_ReticulateAnnData)
- [`anndataR::AbstractAnnData$as_Seurat()`](https://anndataR.data-intuitive.com/reference/AbstractAnnData.html#method-as_Seurat)
- [`anndataR::AbstractAnnData$as_SingleCellExperiment()`](https://anndataR.data-intuitive.com/reference/AbstractAnnData.html#method-as_SingleCellExperiment)
- [`anndataR::AbstractAnnData$layers_keys()`](https://anndataR.data-intuitive.com/reference/AbstractAnnData.html#method-layers_keys)
- [`anndataR::AbstractAnnData$obs_keys()`](https://anndataR.data-intuitive.com/reference/AbstractAnnData.html#method-obs_keys)
- [`anndataR::AbstractAnnData$obsm_keys()`](https://anndataR.data-intuitive.com/reference/AbstractAnnData.html#method-obsm_keys)
- [`anndataR::AbstractAnnData$obsp_keys()`](https://anndataR.data-intuitive.com/reference/AbstractAnnData.html#method-obsp_keys)
- [`anndataR::AbstractAnnData$print()`](https://anndataR.data-intuitive.com/reference/AbstractAnnData.html#method-print)
- [`anndataR::AbstractAnnData$shape()`](https://anndataR.data-intuitive.com/reference/AbstractAnnData.html#method-shape)
- [`anndataR::AbstractAnnData$uns_keys()`](https://anndataR.data-intuitive.com/reference/AbstractAnnData.html#method-uns_keys)
- [`anndataR::AbstractAnnData$var_keys()`](https://anndataR.data-intuitive.com/reference/AbstractAnnData.html#method-var_keys)
- [`anndataR::AbstractAnnData$varm_keys()`](https://anndataR.data-intuitive.com/reference/AbstractAnnData.html#method-varm_keys)
- [`anndataR::AbstractAnnData$varp_keys()`](https://anndataR.data-intuitive.com/reference/AbstractAnnData.html#method-varp_keys)
- [`anndataR::AbstractAnnData$write_h5ad()`](https://anndataR.data-intuitive.com/reference/AbstractAnnData.html#method-write_h5ad)

------------------------------------------------------------------------

### Method `new()`

Close the HDF5 file when the object is garbage collected

`HDF5AnnData` constructor

#### Usage

    HDF5AnnData$new(
      file,
      X = NULL,
      obs = NULL,
      var = NULL,
      layers = NULL,
      obsm = NULL,
      varm = NULL,
      obsp = NULL,
      varp = NULL,
      uns = NULL,
      shape = NULL,
      mode = c("a", "r", "r+", "w", "w-", "x"),
      compression = c("none", "gzip", "lzf")
    )

#### Arguments

- `file`:

  The file name (character) of the `.h5ad` file. If this file already
  exits, other arguments must be `NULL`.

- `X`:

  See the `X` slot in
  [AnnData-usage](https://anndataR.data-intuitive.com/reference/AnnData-usage.md)

- `obs`:

  See the `obs` slot in
  [AnnData-usage](https://anndataR.data-intuitive.com/reference/AnnData-usage.md)

- `var`:

  See the `var` slot in
  [AnnData-usage](https://anndataR.data-intuitive.com/reference/AnnData-usage.md)

- `layers`:

  See the `layers` slot in
  [AnnData-usage](https://anndataR.data-intuitive.com/reference/AnnData-usage.md)

- `obsm`:

  See the `obsm` slot in
  [AnnData-usage](https://anndataR.data-intuitive.com/reference/AnnData-usage.md)

- `varm`:

  See the `varm` slot in
  [AnnData-usage](https://anndataR.data-intuitive.com/reference/AnnData-usage.md)

- `obsp`:

  See the `obsp` slot in
  [AnnData-usage](https://anndataR.data-intuitive.com/reference/AnnData-usage.md)

- `varp`:

  See the `varp` slot in
  [AnnData-usage](https://anndataR.data-intuitive.com/reference/AnnData-usage.md)

- `uns`:

  See the `uns` slot in
  [AnnData-usage](https://anndataR.data-intuitive.com/reference/AnnData-usage.md)

- `shape`:

  Shape tuple (e.g. `c(n_obs, n_vars)`). Can be provided if both `X` or
  `obs` and `var` are not provided.

- `mode`:

  The mode to open the HDF5 file. See
  [`as_HDF5AnnData()`](https://anndataR.data-intuitive.com/reference/as_HDF5AnnData.md)
  for details

- `compression`:

  The compression algorithm to use. See
  [`as_HDF5AnnData()`](https://anndataR.data-intuitive.com/reference/as_HDF5AnnData.md)
  for details

#### Details

The constructor creates a new HDF5 `AnnData` interface object. This can
either be used to either connect to an existing `.h5ad` file or to
create a new one. If any additional slot arguments are set an existing
file will be overwritten.

------------------------------------------------------------------------

### Method [`close()`](https://rdrr.io/r/base/connections.html)

Close the HDF5 file

#### Usage

    HDF5AnnData$close()

------------------------------------------------------------------------

### Method `n_obs()`

See the `n_obs` field in
[AnnData-usage](https://anndataR.data-intuitive.com/reference/AnnData-usage.md)

#### Usage

    HDF5AnnData$n_obs()

------------------------------------------------------------------------

### Method `n_vars()`

See the `n_vars` field in
[AnnData-usage](https://anndataR.data-intuitive.com/reference/AnnData-usage.md)

#### Usage

    HDF5AnnData$n_vars()

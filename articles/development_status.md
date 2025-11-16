# Development status

## Introduction

This vignette provides an overview of the current development status of
the *[anndataR](https://bioconductor.org/packages/3.22/anndataR)*
package. It provides details on the current implementation of different
features as well as listing known issues.

## Objects

These tables show the status of the implementation of different
`AnnData` back ends.

### `HDF5AnnData`

| Slot      |                                  Getter                                  |                                        Getter test                                         |                                  Setter                                  |                                        Setter test                                         |
|:----------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------------------------:|:------------------------------------------------------------------------:|:------------------------------------------------------------------------------------------:|
| layers    | [✅](https://github.com/scverse/anndataR/blob/main/R/HDF5AnnData.R#L74)  | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-HDF5AnnData.R#L23)  | [✅](https://github.com/scverse/anndataR/blob/main/R/HDF5AnnData.R#L78)  | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-HDF5AnnData.R#L146) |
| obs       | [✅](https://github.com/scverse/anndataR/blob/main/R/HDF5AnnData.R#L196) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-HDF5AnnData.R#L73)  | [✅](https://github.com/scverse/anndataR/blob/main/R/HDF5AnnData.R#L199) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-HDF5AnnData.R#L157) |
| obs_names | [✅](https://github.com/scverse/anndataR/blob/main/R/HDF5AnnData.R#L230) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-HDF5AnnData.R#L117) | [✅](https://github.com/scverse/anndataR/blob/main/R/HDF5AnnData.R#L233) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-HDF5AnnData.R#L189) |
| obsm      | [✅](https://github.com/scverse/anndataR/blob/main/R/HDF5AnnData.R#L98)  | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-HDF5AnnData.R#L33)  | [✅](https://github.com/scverse/anndataR/blob/main/R/HDF5AnnData.R#L102) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-HDF5AnnData.R#L211) |
| obsp      | [✅](https://github.com/scverse/anndataR/blob/main/R/HDF5AnnData.R#L148) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-HDF5AnnData.R#L53)  | [✅](https://github.com/scverse/anndataR/blob/main/R/HDF5AnnData.R#L152) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-HDF5AnnData.R#L240) |
| raw       |                                                                          |                                                                                            |                                                                          |                                                                                            |
| uns       | [✅](https://github.com/scverse/anndataR/blob/main/R/HDF5AnnData.R#L254) |                                                                                            | [✅](https://github.com/scverse/anndataR/blob/main/R/HDF5AnnData.R#L257) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-HDF5AnnData.R#L270) |
| var       | [✅](https://github.com/scverse/anndataR/blob/main/R/HDF5AnnData.R#L213) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-HDF5AnnData.R#L95)  | [✅](https://github.com/scverse/anndataR/blob/main/R/HDF5AnnData.R#L216) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-HDF5AnnData.R#L173) |
| var_names | [✅](https://github.com/scverse/anndataR/blob/main/R/HDF5AnnData.R#L242) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-HDF5AnnData.R#L123) | [✅](https://github.com/scverse/anndataR/blob/main/R/HDF5AnnData.R#L245) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-HDF5AnnData.R#L200) |
| varm      | [✅](https://github.com/scverse/anndataR/blob/main/R/HDF5AnnData.R#L123) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-HDF5AnnData.R#L43)  | [✅](https://github.com/scverse/anndataR/blob/main/R/HDF5AnnData.R#L127) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-HDF5AnnData.R#L226) |
| varp      | [✅](https://github.com/scverse/anndataR/blob/main/R/HDF5AnnData.R#L172) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-HDF5AnnData.R#L63)  | [✅](https://github.com/scverse/anndataR/blob/main/R/HDF5AnnData.R#L176) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-HDF5AnnData.R#L255) |
| X         | [✅](https://github.com/scverse/anndataR/blob/main/R/HDF5AnnData.R#L50)  | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-HDF5AnnData.R#L16)  | [✅](https://github.com/scverse/anndataR/blob/main/R/HDF5AnnData.R#L54)  | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-HDF5AnnData.R#L135) |

### `InMemoryAnnData`

| Slot      |                                    Getter                                    |                                          Getter test                                          |                                    Setter                                    |                                          Setter test                                           |
|:----------|:----------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|:----------------------------------------------------------------------------------------------:|
| layers    | [✅](https://github.com/scverse/anndataR/blob/main/R/InMemoryAnnData.R#L75)  | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-InMemoryAnnData.R#L55) | [✅](https://github.com/scverse/anndataR/blob/main/R/InMemoryAnnData.R#L79)  | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-InMemoryAnnData.R#L248) |
| obs       | [✅](https://github.com/scverse/anndataR/blob/main/R/InMemoryAnnData.R#L93)  | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-InMemoryAnnData.R#L16) | [✅](https://github.com/scverse/anndataR/blob/main/R/InMemoryAnnData.R#L97)  | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-InMemoryAnnData.R#L148) |
| obs_names | [✅](https://github.com/scverse/anndataR/blob/main/R/InMemoryAnnData.R#L127) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-InMemoryAnnData.R#L20) | [✅](https://github.com/scverse/anndataR/blob/main/R/InMemoryAnnData.R#L130) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-InMemoryAnnData.R#L212) |
| obsm      | [✅](https://github.com/scverse/anndataR/blob/main/R/InMemoryAnnData.R#L149) |                                                                                               | [✅](https://github.com/scverse/anndataR/blob/main/R/InMemoryAnnData.R#L153) |                                                                                                |
| obsp      | [✅](https://github.com/scverse/anndataR/blob/main/R/InMemoryAnnData.R#L187) |                                                                                               | [✅](https://github.com/scverse/anndataR/blob/main/R/InMemoryAnnData.R#L191) |                                                                                                |
| raw       |                                                                              |                                                                                               |                                                                              |                                                                                                |
| uns       | [✅](https://github.com/scverse/anndataR/blob/main/R/InMemoryAnnData.R#L223) |                                                                                               | [✅](https://github.com/scverse/anndataR/blob/main/R/InMemoryAnnData.R#L226) |                                                                                                |
| var       | [✅](https://github.com/scverse/anndataR/blob/main/R/InMemoryAnnData.R#L110) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-InMemoryAnnData.R#L18) | [✅](https://github.com/scverse/anndataR/blob/main/R/InMemoryAnnData.R#L114) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-InMemoryAnnData.R#L180) |
| var_names | [✅](https://github.com/scverse/anndataR/blob/main/R/InMemoryAnnData.R#L138) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-InMemoryAnnData.R#L22) | [✅](https://github.com/scverse/anndataR/blob/main/R/InMemoryAnnData.R#L141) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-InMemoryAnnData.R#L230) |
| varm      | [✅](https://github.com/scverse/anndataR/blob/main/R/InMemoryAnnData.R#L168) |                                                                                               | [✅](https://github.com/scverse/anndataR/blob/main/R/InMemoryAnnData.R#L172) |                                                                                                |
| varp      | [✅](https://github.com/scverse/anndataR/blob/main/R/InMemoryAnnData.R#L205) |                                                                                               | [✅](https://github.com/scverse/anndataR/blob/main/R/InMemoryAnnData.R#L209) |                                                                                                |
| X         | [✅](https://github.com/scverse/anndataR/blob/main/R/InMemoryAnnData.R#L57)  | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-InMemoryAnnData.R#L11) | [✅](https://github.com/scverse/anndataR/blob/main/R/InMemoryAnnData.R#L61)  | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-InMemoryAnnData.R#L119) |

### `ReticulateAnnData`

| Slot      |                                     Getter                                     |                                           Getter test                                            |                                     Setter                                     |                                           Setter test                                            |
|:----------|:------------------------------------------------------------------------------:|:------------------------------------------------------------------------------------------------:|:------------------------------------------------------------------------------:|:------------------------------------------------------------------------------------------------:|
| layers    | [✅](https://github.com/scverse/anndataR/blob/main/R/ReticulateAnnData.R#L57)  | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-ReticulateAnnData.R#L84)  | [✅](https://github.com/scverse/anndataR/blob/main/R/ReticulateAnnData.R#L72)  | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-ReticulateAnnData.R#L254) |
| obs       | [✅](https://github.com/scverse/anndataR/blob/main/R/ReticulateAnnData.R#L90)  | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-ReticulateAnnData.R#L74)  | [✅](https://github.com/scverse/anndataR/blob/main/R/ReticulateAnnData.R#L93)  | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-ReticulateAnnData.R#L112) |
| obs_names | [✅](https://github.com/scverse/anndataR/blob/main/R/ReticulateAnnData.R#L120) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-ReticulateAnnData.R#L94)  | [✅](https://github.com/scverse/anndataR/blob/main/R/ReticulateAnnData.R#L127) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-ReticulateAnnData.R#L235) |
| obsm      | [✅](https://github.com/scverse/anndataR/blob/main/R/ReticulateAnnData.R#L164) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-ReticulateAnnData.R#L169) | [✅](https://github.com/scverse/anndataR/blob/main/R/ReticulateAnnData.R#L167) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-ReticulateAnnData.R#L200) |
| obsp      | [✅](https://github.com/scverse/anndataR/blob/main/R/ReticulateAnnData.R#L204) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-ReticulateAnnData.R#L181) | [✅](https://github.com/scverse/anndataR/blob/main/R/ReticulateAnnData.R#L207) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-ReticulateAnnData.R#L214) |
| uns       | [✅](https://github.com/scverse/anndataR/blob/main/R/ReticulateAnnData.R#L246) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-ReticulateAnnData.R#L89)  | [✅](https://github.com/scverse/anndataR/blob/main/R/ReticulateAnnData.R#L249) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-ReticulateAnnData.R#L132) |
| var       | [✅](https://github.com/scverse/anndataR/blob/main/R/ReticulateAnnData.R#L105) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-ReticulateAnnData.R#L79)  | [✅](https://github.com/scverse/anndataR/blob/main/R/ReticulateAnnData.R#L108) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-ReticulateAnnData.R#L122) |
| var_names | [✅](https://github.com/scverse/anndataR/blob/main/R/ReticulateAnnData.R#L142) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-ReticulateAnnData.R#L96)  | [✅](https://github.com/scverse/anndataR/blob/main/R/ReticulateAnnData.R#L149) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-ReticulateAnnData.R#L241) |
| varm      | [✅](https://github.com/scverse/anndataR/blob/main/R/ReticulateAnnData.R#L184) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-ReticulateAnnData.R#L175) | [✅](https://github.com/scverse/anndataR/blob/main/R/ReticulateAnnData.R#L187) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-ReticulateAnnData.R#L207) |
| varp      | [✅](https://github.com/scverse/anndataR/blob/main/R/ReticulateAnnData.R#L225) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-ReticulateAnnData.R#L187) | [✅](https://github.com/scverse/anndataR/blob/main/R/ReticulateAnnData.R#L228) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-ReticulateAnnData.R#L221) |
| X         | [✅](https://github.com/scverse/anndataR/blob/main/R/ReticulateAnnData.R#L36)  | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-ReticulateAnnData.R#L70)  | [✅](https://github.com/scverse/anndataR/blob/main/R/ReticulateAnnData.R#L39)  | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-ReticulateAnnData.R#L106) |

## Conversion

These tables show the implementation status of conversion between
`AnnData` and other objects.

### `SingleCellExperiment`

| Slot      |                                          From                                          |                                                From test                                                 |                                          To                                          |                                                To test                                                 |
|:----------|:--------------------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------------------------:|:------------------------------------------------------------------------------------:|:------------------------------------------------------------------------------------------------------:|
| layers    | [✅](https://github.com/scverse/anndataR/blob/main/R/from_SingleCellExperiment.R#L262) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-from_SingleCellExperiment.R#L66)  | [✅](https://github.com/scverse/anndataR/blob/main/R/as_SingleCellExperiment.R#L209) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-as_SingleCellExperiment.R#L64)  |
| obs       | [✅](https://github.com/scverse/anndataR/blob/main/R/from_SingleCellExperiment.R#L214) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-from_SingleCellExperiment.R#L24)  | [✅](https://github.com/scverse/anndataR/blob/main/R/as_SingleCellExperiment.R#L239) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-as_SingleCellExperiment.R#L22)  |
| obs_names | [✅](https://github.com/scverse/anndataR/blob/main/R/from_SingleCellExperiment.R#L213) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-from_SingleCellExperiment.R#L18)  | [✅](https://github.com/scverse/anndataR/blob/main/R/as_SingleCellExperiment.R#L240) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-as_SingleCellExperiment.R#L18)  |
| obsm      | [✅](https://github.com/scverse/anndataR/blob/main/R/from_SingleCellExperiment.R#L275) | [🚧](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-from_SingleCellExperiment.R#L176) | [✅](https://github.com/scverse/anndataR/blob/main/R/as_SingleCellExperiment.R#L347) | [🚧](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-as_SingleCellExperiment.R#L202) |
| obsp      | [✅](https://github.com/scverse/anndataR/blob/main/R/from_SingleCellExperiment.R#L339) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-from_SingleCellExperiment.R#L90)  | [✅](https://github.com/scverse/anndataR/blob/main/R/as_SingleCellExperiment.R#L249) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-as_SingleCellExperiment.R#L123) |
| raw       |                                                                                        |                                                                                                          |                                                                                      |                                                                                                        |
| uns       | [✅](https://github.com/scverse/anndataR/blob/main/R/from_SingleCellExperiment.R#L387) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-from_SingleCellExperiment.R#L145) | [✅](https://github.com/scverse/anndataR/blob/main/R/as_SingleCellExperiment.R#L257) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-as_SingleCellExperiment.R#L171) |
| var       | [✅](https://github.com/scverse/anndataR/blob/main/R/from_SingleCellExperiment.R#L238) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-from_SingleCellExperiment.R#L45)  | [✅](https://github.com/scverse/anndataR/blob/main/R/as_SingleCellExperiment.R#L244) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-as_SingleCellExperiment.R#L43)  |
| var_names | [✅](https://github.com/scverse/anndataR/blob/main/R/from_SingleCellExperiment.R#L237) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-from_SingleCellExperiment.R#L20)  | [✅](https://github.com/scverse/anndataR/blob/main/R/as_SingleCellExperiment.R#L245) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-as_SingleCellExperiment.R#L16)  |
| varm      | [✅](https://github.com/scverse/anndataR/blob/main/R/from_SingleCellExperiment.R#L301) | [🚧](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-from_SingleCellExperiment.R#L183) | [✅](https://github.com/scverse/anndataR/blob/main/R/as_SingleCellExperiment.R#L348) | [🚧](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-as_SingleCellExperiment.R#L210) |
| varp      | [✅](https://github.com/scverse/anndataR/blob/main/R/from_SingleCellExperiment.R#L363) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-from_SingleCellExperiment.R#L118) | [✅](https://github.com/scverse/anndataR/blob/main/R/as_SingleCellExperiment.R#L253) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-as_SingleCellExperiment.R#L147) |
| X         | [✅](https://github.com/scverse/anndataR/blob/main/R/from_SingleCellExperiment.R#L111) |                                                                                                          | [✅](https://github.com/scverse/anndataR/blob/main/R/as_SingleCellExperiment.R#L208) |                                                                                                        |

### `Seurat`

| Slot      |                                   From                                   |                                         From test                                          |                                   To                                   |                                         To test                                          |
|:----------|:------------------------------------------------------------------------:|:------------------------------------------------------------------------------------------:|:----------------------------------------------------------------------:|:----------------------------------------------------------------------------------------:|
| layers    | [✅](https://github.com/scverse/anndataR/blob/main/R/from_Seurat.R#L236) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-from_Seurat.R#L73)  | [✅](https://github.com/scverse/anndataR/blob/main/R/as_Seurat.R#L219) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-as_Seurat.R#L74)  |
| obs       | [✅](https://github.com/scverse/anndataR/blob/main/R/from_Seurat.R#L184) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-from_Seurat.R#L35)  | [✅](https://github.com/scverse/anndataR/blob/main/R/as_Seurat.R#L211) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-as_Seurat.R#L33)  |
| obs_names | [✅](https://github.com/scverse/anndataR/blob/main/R/from_Seurat.R#L183) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-from_Seurat.R#L31)  | [✅](https://github.com/scverse/anndataR/blob/main/R/as_Seurat.R#L242) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-as_Seurat.R#L29)  |
| obsm      | [✅](https://github.com/scverse/anndataR/blob/main/R/from_Seurat.R#L265) | [🚧](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-from_Seurat.R#L124) | [✅](https://github.com/scverse/anndataR/blob/main/R/as_Seurat.R#L501) | [🚧](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-as_Seurat.R#L127) |
| obsp      | [✅](https://github.com/scverse/anndataR/blob/main/R/from_Seurat.R#L335) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-from_Seurat.R#L170) | [✅](https://github.com/scverse/anndataR/blob/main/R/as_Seurat.R#L258) |                                                                                          |
| raw       |                                                                          |                                                                                            |                                                                        |                                                                                          |
| uns       | [✅](https://github.com/scverse/anndataR/blob/main/R/from_Seurat.R#L408) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-from_Seurat.R#L97)  | [✅](https://github.com/scverse/anndataR/blob/main/R/as_Seurat.R#L279) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-as_Seurat.R#L99)  |
| var       | [✅](https://github.com/scverse/anndataR/blob/main/R/from_Seurat.R#L211) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-from_Seurat.R#L56)  | [✅](https://github.com/scverse/anndataR/blob/main/R/as_Seurat.R#L227) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-as_Seurat.R#L55)  |
| var_names | [✅](https://github.com/scverse/anndataR/blob/main/R/from_Seurat.R#L210) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-from_Seurat.R#L29)  | [✅](https://github.com/scverse/anndataR/blob/main/R/as_Seurat.R#L243) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-as_Seurat.R#L27)  |
| varm      | [✅](https://github.com/scverse/anndataR/blob/main/R/from_Seurat.R#L295) | [✅](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-from_Seurat.R#L131) | [✅](https://github.com/scverse/anndataR/blob/main/R/as_Seurat.R#L502) | [🚧](https://github.com/scverse/anndataR/blob/main/tests/testthat/test-as_Seurat.R#L135) |
| varp      | [✅](https://github.com/scverse/anndataR/blob/main/R/from_Seurat.R#L371) |                                                                                            |                                                                        |                                                                                          |
| X         | [✅](https://github.com/scverse/anndataR/blob/main/R/from_Seurat.R#L133) |                                                                                            | [✅](https://github.com/scverse/anndataR/blob/main/R/as_Seurat.R#L218) |                                                                                          |

## Known issues

This section lists current known issues in
*[anndataR](https://bioconductor.org/packages/3.22/anndataR)*. Only
certain types of issues are listed here, for additional issues see the
[GitHub issue
tracker](https://github.com/scverse/anndataR/issues?q=sort%3Aupdated-desc+is%3Aissue+is%3Aopen).

### Issue: converted sce object has dimnames(), whilst the original anndata does not.

- Affected backend: `to_SCE`
- Affected slot(s): `obsm`, `varm`
- Affected dtype(s): `pca`
- Probable cause: convert
- To investigate: TRUE
- To fix: FALSE

#### Error message

    sampleFactors(reducedDims(sce)$pca) (`actual`) not equal to ad$obsm[["X_pca"]] (`expected`).
    `dimnames(actual)` is a list `dimnames(expected)` is absent

#### Proposed solution

Investigate if this is a problem or not.

## Session info

``` r
sessionInfo()
```

    ## R version 4.5.2 (2025-10-31)
    ## Platform: x86_64-pc-linux-gnu
    ## Running under: Ubuntu 24.04.3 LTS
    ## 
    ## Matrix products: default
    ## BLAS:   /usr/lib/x86_64-linux-gnu/openblas-pthread/libblas.so.3 
    ## LAPACK: /usr/lib/x86_64-linux-gnu/openblas-pthread/libopenblasp-r0.3.26.so;  LAPACK version 3.12.0
    ## 
    ## locale:
    ##  [1] LC_CTYPE=C.UTF-8       LC_NUMERIC=C           LC_TIME=C.UTF-8       
    ##  [4] LC_COLLATE=C.UTF-8     LC_MONETARY=C.UTF-8    LC_MESSAGES=C.UTF-8   
    ##  [7] LC_PAPER=C.UTF-8       LC_NAME=C              LC_ADDRESS=C          
    ## [10] LC_TELEPHONE=C         LC_MEASUREMENT=C.UTF-8 LC_IDENTIFICATION=C   
    ## 
    ## time zone: UTC
    ## tzcode source: system (glibc)
    ## 
    ## attached base packages:
    ## [1] stats     graphics  grDevices utils     datasets  methods   base     
    ## 
    ## other attached packages:
    ## [1] tidyr_1.3.1      dplyr_1.1.4      purrr_1.2.0      stringr_1.6.0   
    ## [5] rprojroot_2.1.1  knitr_1.50       tibble_3.3.0     BiocStyle_2.38.0
    ## 
    ## loaded via a namespace (and not attached):
    ##  [1] vctrs_0.6.5         cli_3.6.5           rlang_1.1.6        
    ##  [4] xfun_0.54           stringi_1.8.7       generics_0.1.4     
    ##  [7] textshaping_1.0.4   jsonlite_2.0.0      glue_1.8.0         
    ## [10] htmltools_0.5.8.1   ragg_1.5.0          sass_0.4.10        
    ## [13] rmarkdown_2.30      evaluate_1.0.5      jquerylib_0.1.4    
    ## [16] fastmap_1.2.0       yaml_2.3.10         lifecycle_1.0.4    
    ## [19] bookdown_0.45       BiocManager_1.30.26 compiler_4.5.2     
    ## [22] fs_1.6.6            pkgconfig_2.0.3     htmlwidgets_1.6.4  
    ## [25] systemfonts_1.3.1   digest_0.6.38       R6_2.6.1           
    ## [28] tidyselect_1.2.1    pillar_1.11.1       magrittr_2.0.4     
    ## [31] bslib_0.9.0         withr_3.0.2         tools_4.5.2        
    ## [34] pkgdown_2.2.0       cachem_1.1.0        desc_1.4.3

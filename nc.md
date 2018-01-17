# nc

## identifier
| type              | value
| ----------------- | -----
| alias             | [Network Common Data Form](#network-common-data-form)
| alias             | [NetCDF](#network-common-data-form)
| alias             | [netCDF-3](#netcdf-3)
| alias             | [netCDF-4](#netcdf-4)
| alias             | [Parallel-NetCDF](#parallel-netcdf)

# Network Common Data Form
The `Network Common Data Form` refers both to a format, an interface and a program that implements the interface. The first program was a re-implementation of the program for [CDF](cdf.md) but ["NetCDF and CDF have evolved independently."](https://www.unidata.ucar.edu/software/netcdf/docs/faq.html#What-is-the-connection-between-netCDF-and-CDF).

## identifier
| type                    | value
| ----------------------- | -----
| file extension          | nc
| file extension          | cdf <sup>**[1]**</sup>

> **[1]** The recommended extension for netCDF files was changed from ".cdf" to ".nc" in 1994 in order to avoid a clash with the NASA CDF file extension, and now it also avoids confusion with "Channel Definition Format" files. `NetCDF  4.5.0` [FAQ](https://www.unidata.ucar.edu/software/netcdf/docs/faq.html#What-convention-should-be-used-for-the-names-of-netCDF-files) (20180111).

## netCDF-4
NetCDF-4 is an informal reference to either [netCDF-4 format](#netcdf-4-format) or [netCDF-4 classic model format](#netcdf-4-classic-model-format).

## NetCDF-4 Format
### identifier
| type                    | value
| ----------------------- | -----
| informal                | [NetCDF-4](#netcdf-4)
| signature               | `\211HDF`
| signature               | `\211HDF\r\n\032\n`

### source
| reference | note
| --------- | ----
| NetCDF Documentation | [20171018](https://www.unidata.ucar.edu/software/netcdf/docs/index.html)
| Unidata -- NetCDF | v4.5.0, [Appendix B. The NetCDF-4 Format](https://www.unidata.ucar.edu/software/netcdf/docs/file_format_specifications.html#netcdf_4_spec).

#### NetCDF 4.5.0
| format | requirement | reference | note
| ------ | ----------- | --------- | ----
| [HDF5](hdf.md#hdf5) | | superset | The HDF Group -- [HDF5](https://support.hdfgroup.org/HDF5/doc/index.html) | v1.8 and later. NetCDF applies a limited subset of HDF5.

## NetCDF-4 Classic Model Format
### identifier
| type                    | value
| ----------------------- | -----
| informal                | NetCDF-4
| signature               | `\211HDF`
| signature               | `\211HDF\r\n\032\n`

### source
| reference | note
| --------- | ----
| NetCDF Documentation | [20171018](https://www.unidata.ucar.edu/software/netcdf/docs/index.html)
| Unidata -- NetCDF | v4.5.0, [Appendix B. The NetCDF-4 Classic Model Format](https://www.unidata.ucar.edu/software/netcdf/docs/file_format_specifications.html#netcdf_4_classic_spec).

## netCDF-3
NetCDF-3 is an informal reference to data format created by the code library `netCDF-3`, `netCDF-2`, or `netCDF-1`. The data format however is either [netCDF classic format](#netcdf-classic-format) or [netCDF 64-bit offset format](#netcdf-64-bit-offset-format).

## netCDF classic format
### identifier
| type                    | value
| ----------------------- | -----
| informal                | [netCDF-3](#netcdf-3)
| signature               | `CDF\001`

### source
| reference | note
| --------- | ----
| NetCDF Documentation | [20171018](https://www.unidata.ucar.edu/software/netcdf/docs/index.html)
| Unidata -- NetCDF | v4.5.0, [Appendix B. The NetCDF Classic Format Specification](https://www.unidata.ucar.edu/software/netcdf/docs/file_format_specifications.html#classic_format_spec).

## netCDF 64-bit offset format
### identifier
| type                    | value
| ----------------------- | -----
| informal                | [netCDF-3](#netcdf-3)
| signature               | `CDF\002`

Except for the `OFFSET` entity at `64-bit` instead of `32-bit`, the `netCDF 64-bit offset` format is exactly the same as [netCDF classic format](#netcdf-classic-format).

| reference | note
| --------- | ----
| NetCDF Documentation | [20171018](https://www.unidata.ucar.edu/software/netcdf/docs/index.html)
| Unidata -- NetCDF | v4.5.0, [Appendix B. The 64-bit Offset Format](https://www.unidata.ucar.edu/software/netcdf/docs/file_format_specifications.html#offset_format_spec).

# Parallel NetCDF
[Parallel netCDF](https://trac.mcs.anl.gov/projects/parallel-netcdf) is a Parallel `I/O` library for accessing [NetCDF-3](#netcdf-3) Files in either [netCDF classic format](#netcdf-classic-format) or [netCDF 64-bit offset format](#netcdf-64-bit-offset-format).

| type | value
| ---- | -----
| alias | PnetCDF

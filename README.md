ansible-gdal-netcdf
===================

An ansible role for install GDAL with python bindings that allow the library to work with netCDF files. The versions of the HDF5, netCDF, and GDAL library are specifically set to work with the NASA NEX Downscaled Climate Projections dataset (http://aws.amazon.com/nasa/nex/). There was an issue dealing with the various versions on the libraries and how they functioned on a Macbook and Ubuntu machines (see http://gis.stackexchange.com/questions/130705/gdal-reads-nex-climate-projection-datasets-as-netcdf-on-mac-hdf5-on-ubuntu/131105#131105), and these version specifically solve that issue. There is probably other versioning that would work (i.e. GDAL might not have to be that specific commit), but this combination is proven to work.

Role Variables
--------------

- `install_dir`: Directory to download sources to during the build process.

Other variables in the [defaults]`defaults/main.yml` have to do with the versioning of each of the libraries. Change at your own peril.

Dependencies
------------

This role requires build-essentails, python-dev and git be installed.

Example Playbook
----------------

See the [examples](./examples/) directory.

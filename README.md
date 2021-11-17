# tephra2-inversion
inversion using the tephra2 forward model and the downhill simplex method

To run the inversion model, at the command line, type:
```
mpirun -np nodes -hostfile machines tephra2-inversion_2020 tepha2-inversion.conf data_file wind_file
```
where,
- **mpirun** is the wrapper script for *gcc* when using mpi libraries
- **nodes** is the number of cluster compute nodes to use
- **machines** is a text file listing the name of each compute node and the number of cpu cores useable on that node ([an example](inputs/machines))
- **tephra2-inversion_2020** is the executable name
- **tephra2-inversion.conf** is the file of parameters ([an example](inputs/tephra2-inversion.conf))
- **data_file** is a text file of tephra accumulation data from chosen area ([an example](inputs/colima_59wgs84z13.xyz)) following the format:
    ```
    Easting(m)  Northing(m)  Grid-elevation(m)  Mass(kg/m^2)
    ```
- **wind_file** is a text file of wind data to use for the inversion 

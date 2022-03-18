# Peter's Regridding Repository

The idea of the scripts in this repository are to regrid MODIS SST L2 fields to address the bowtie effect.  

## Here are the first few lines of the function that does this. 

[new_lon, new_sst, new_flags, new_qual, new_sstref, region_start, region_end, easting, northing] = regrid_MODIS_orbits( ...
    longitude, latitude, SST_In, flags_sst, Qual_In, sstref)
    
%  regrid_MODIS_orbits - regrid MODIS orbit - PCC

%
% INPUT
%   longitude - array to be fixed.
%   latitude - needed for high latitude locations.
%   base_dir_out - the directory to which the new lon, lat, SST_In and mask
%    will be writte. The output filename will the same as the input filename
%    with '_fixed' appended.
%
% EXAMPLE
%   fi_in = '~/Dropbox/Data/Fronts_test/MODIS_Aqua_L2/Original/2010/AQUA_MODIS.20100619T000124.L2.SST.mat';
%   regrid_MODIS_orbits( fi_in, [])

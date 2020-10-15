# FM System of Numbering WMO CF-NetCDF Profiles

## FM System of Numbering WMO CF-NetCDF Profiles

- Introductory paragraph describing numbering scheme
- Notes of nomenclature
- Table listing profiles
- WMO namespace to avoid future collision

### Representation of information in WMO CF-NetCDF

In this section we describe how we extend the CF conventions.

### NetCDF version
- Should be NetCDF4 (strong recommendation vs mandatory)
- Need to be aware of backwards compatibility and those using older systems
- extension .nc

### Naming conventions
- case is significant, CF makes no recommendation
- WMO-CF extends by making lower snake case mandatory?

### Dimensions
- For gridded data with x, y, z and t as dimensions CF recommends order but this is not mandatory.
- WMO CF extends by making ordering mandatory
- Similarly, where other dimensions used mandatory ordering specified by WMO CF
- This will be based on the profile / feature type
- Other dimensions shall appear to the left
- CF does not standardise dimensions names, WMO CF does

### Variables - general requirements
Attributes defined in NUG, made mandatory under WMO CF:
- standard_name - should be used where they exist but optional
- _FillValue, should (not shall) be used. In some cases full width required for data and no space for fill value (note - does this suggest we need a wider width?)
- valid_min and valid_max mandatory
- scale_factor, add_offset mandatory or optional ()?

The following new attributes defined for unambiguous identification of variables and units:
- wmo_parameter_uri
- wmo_parameter_name (mandatory use for variable name? shorter than CF standard names)
- wmo_unit_uri
- wmo_unit_name

### Coordinate variables
Dependence on feature type
- gridded data
- discrete geometries
- axis attribute following CF conventions

### Geophysical variables
- attributes as above and following CF conventions for discrete geometries
- attribute linking to ancillary variables


### Ancillary variables
- equivalent to significance qualifiers
- include meaning of codes / flags in attribute
- bit flags?

### Quality control information
- should / shall include QC information
- encoding of QC information

### Character storage encoding
- string vs char
- dimension names

### Global attributes / header information
- language
- feature type
- other CF attributes
- WMO attributes, e.g. originating centre, typical time of message contents etc

### Packing, chunking and compression
- scale_factor
- add_offset
- chunking 
- compression

## Tables and lists supporting the WMO CF Conventions
e.g. http://codes.wmo.int/

## References

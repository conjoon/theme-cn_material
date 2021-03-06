# theme-cn_material  
This **Sencha ExtJS** package contains the material theme for development of [conjoon](https://github.com/conjoon) along
with its application packages.
Please note, that this theme serves as a base for pluggable packages, such as 
[conjoon/app-cn_mail](https://github.com/conjoon/app-cn_mail), where styling information for these 
packages are self-contained.
This theme extends the Material-Theme of ExtJS. ExtJS > 7.0 is required for this package. 


## Naming
The following naming conventions apply:

#### Namespace
#### Package name
`theme-cn_material`

# Usage
## Requirements

# Usage
Specified as ```theme``` property in conjoon's ```app.json```.
Additionally, packages providing styling information might refer to this theme
to access SASS-variable definitions.

# Note
## Registering as a coon.js-Theme
This theme automatically registers itself by setting the following global properties:
```
Ext.theme.is["coon-js-theme"] = true;
Ext.theme.name = "theme-cn_material";
```
This is to identify itself later on for proper inclusion in the coon.js-environment.

## Loading Source Files
Although the package is registered as a static-theme package, sources such as the ```conjoon.theme.material.Theme```
cannot be required in a production build if not specified via the ```overrides```-section (instead of 
the ```classpath```-section) - Production-builds simply do not consider sources residing in in the ```classpath``` specified 
in the ```package.json``` (Sencha Cmd v7.3.0.19). 
Thus, this package registers no classpath and uses the ```overrides```-setting instead to make sure all sources
are made available to the owning application.
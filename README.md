# coneToCell
Author: Carlos Arboleda  <br>
Contact: <br>
email (UGent): carlosemilio.arboledachavez@ugent.be  <br>
email (Personal): car_boleda@hotmail.com

coneToCell function for openFoam/foam-extend usage

After file download:

    cd coneToCell
    wclean && wmake libso

Once compilation is over add the following to the system/controlDict file:

    libs
      (
        "libMeshTools.so"
      );
  
Usage in system/setFieldsDict:

    coneToCell

    {
      fieldValues
        (
          volScalarFieldValue  porosityIndex  1
          volVectorFieldValue  U (0.000000 0.000000 0.000000)
        );
      p1 (2.25 1.0 0.0);
      p2 (2.25 1.0 0.12300000000000001);
      radius1 0.45326056233274303; // lower scour protection radius 
      radius2 0.346739437667257; // upper scour protection radius

    }

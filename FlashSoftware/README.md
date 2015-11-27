## This is the Software to generate the *.hex* file for sensorboard with breakout

## Idea
The software should have a button to load the *.hex* file containing the firmware to flash.  
For every generated firmware there should be an JSON file describing the variables one
can edit in the flash storage.

In the software, one loads the *.hex* file containing the firmware and the JSON file.
With the JSON file the software can present a list of variables the user can edit.  
Then the user can click a *save* button to generate a new *.hex* file with the firmware
and the variables.  
This file can now be flashed.

## UI design
![UI design](https://raw.githubusercontent.com/NicoZellinger/SensorMonitoring/master/FlashSoftware/ui-design_v1.png)

### Description
Every variable has a id (the variable name in the firmware), an real name, a type to do typechecking when user edits
and an offset to the base address where this variable is written in the *.hex* file or flash.

Would be nice in the future to generate the JSON file out of the sourcecode directly.  
This could be achieved by marking a section with the variables with code comments.  
The offset can be calculated with the pointer address. The name can be specified by comment and the
type can be obtained out of the code.

## SPEC
Here is an example for the JSON files which describe the variables one can edit:  
[http://www.jsoneditoronline.org/?id=5f7bb21513ac1fcfc43e39b30b590ad5](http://www.jsoneditoronline.org/?id=5f7bb21513ac1fcfc43e39b30b590ad5)

## What is it?
It is an object oriented data model that contains information about different parts of an enterprise. Utilising [WMI](WMI.md) developer can utilise CIM to create "classes" that can represent a wide range of technologies within a company (E.g. router, application, hard disk drive).
## How does it work
An example of CIM in operation is as follows:
1. Manager query CIM class representing a desktop
2. Manager runs script to modify CIM worksatation instance
3. WMI translates any change to CIM class instance into a change on the actual workstation
## Levels of CIM classes
1. Core -Represent managed objects that apply to all areas of management. Examples include `_Parameters` and `_SystemSecurity`.
2. Common - Represent managed objects that apply to specific management areas. Common classes are an extension of core classes. An example is `CIM_UnitaryComputerSystem`
3. Extended - Represent objects that are technology-specific. additions. Typically apply to specific platforms. The `Win32_computerSystem` class is an example
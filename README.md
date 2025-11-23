
# ItemRenamer
A Synthesis Patcher for Fallout 4 that adjusts item names to match those specified in one or more user configurable files, usually to facilitate better inventory sorting.

A default config file is provided with support for FJX-Imperium and MCPR 300. Use it as base to future renamings.

# Current List of Supported Mods
- MW2022 - MCPR 300 - Barrett MRAD
- MW2022 - FJX-Imperium

# Supported record types
- Weapons (`IWeaponGetter`)
- Ammunition (`IAmmunitionGetter`)
- Armor (`IArmorGetter`)
- Books (`IBookGetter`)
- Object Modifications (`IAObjectModificationGetter`)
- Components (`IComponentGetter`)
- Misc items (`IMiscItemGetter`)

# Configuration
To add suport for additional mods, or to change a name definition, simply create one or more json files in the patcher data directory, and they will be read in alphabetical order by file name.
For instance, you could create a file called CustomRules.json in the ```C:/../Synthesis/Data/Fallout 4/ItemRenamer``` directory.

If, for instance, you wanted to change the name of the 10mm item from Gold to 10mm Cool Pistol, you could put:

```"004822:Fallout4.esm": "10mm Cool Pistol",```

on a line in that file, along with the opening and closing JSON braces. In this case, 004822 is the FormID of the 10mm item as seen in xEdit, without the load order index, and Fallout4.esm is the plugin or master file where the item was originally defined. Finally the last part of the line is what you would like to rename the item to. Finally, don't forget to add commas after all lines except the last, as well as opening and closing curly braces to each file.

You can browse the rules included in Default folder in the patcher data folder for more examples.

# LabVIEW QuickDrops Manager

<a href="https://www.vipm.io/package/labview_quickdrops_manager/"> <img src="https://www.vipm.io/package/labview_quickdrops_manager/badge.svg?metric=installs"></a> <a href="https://www.vipm.io/package/labview_quickdrops_manager/"><img src="https://www.vipm.io/package/labview_quickdrops_manager/badge.svg?metric=stars"></a>
[![Check_Broken_VIs](https://github.com/NEVSTOP-LAB/LabVIEW-QuickDrops-Manager/actions/workflows/Check_Broken_VIs.yml/badge.svg)](https://github.com/NEVSTOP-LAB/LabVIEW-QuickDrops-Manager/actions/workflows/Check_Broken_VIs.yml)
[![Build_VIPM_Library](https://github.com/NEVSTOP-LAB/LabVIEW-QuickDrops-Manager/actions/workflows/Build_VIPM_Library.yml/badge.svg)](https://github.com/NEVSTOP-LAB/LabVIEW-QuickDrops-Manager/actions/workflows/Build_VIPM_Library.yml)
[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)



"NI LabVIEW palettes contain hundreds of useful VIs and functions, but, when you know the exact VI you need, navigating through the palette can take too much time. Quick Drop lets you rapidly find and place LabVIEW front panel and block diagram objects without navigating the palettes or initiating a search."

-- [Boost Productivity with Quick Drop](https://www.ni.com/en/support/documentation/supplemental/08/boost-labview-productivity-with-quick-drop.html)

## Ctrl+Q QuickDrop Manager

![image](https://user-images.githubusercontent.com/8196752/82533027-11c7b100-9b75-11ea-9739-a7f55656611a.png)

### Feature

1. Drag form QD list to key to change key assignment.
2. No need to Assign key to every QD, to support all your installed QDs. Type key words to execute QD.
3. QD usage Count.

## Development Environment

- LabVEW 2014
- VIPM 2020.3

### Dependencies

- [OpenG Libraries](http://sine.ni.com/nips/cds/view/p/lang/zhs/nid/209027)
- [MGI Libraries](https://www.vipm.io/package/mgi_lib_mgi_library/)

### Default Key-QD Mapping

`A` --> `[Ctrl]` Align and Distribute</br>
`B` --> `[Ctrl]` Build Array of References</br>
`C` --> _Reserved_</br>
`D` --> `[LabVIEW Build-in]` `[Ctrl]` Wire All Terminals</br>
`E` --> `[Ctrl]` Erease Data(Clear Data)</br>
`F` --> `[Ctrl]` Arrange VI Window</br>
`G` --> `[Ctrl]` `[Shift]` Create a Place VI Contents</br>
`H` --> _Reserved_</br>
`I` --> `[LabVIEW Build-in]` `[Ctrl]` `[Shift]` Insert</br>
`J` --> _Reserved_</br>
`K` --> _Reserved_</br>
`L` --> _Reserved_</br>
`M` --> _Reserved_</br>
`N` --> _Reserved_</br>
`O` --> `[Ctrl]` Smart Open VI Location in Explorer Window</br>
`P` --> `[LabVIEW Build-in]` `[Ctrl]` Replace</br>
`Q` --> `[Ctrl]` NEVSTOP QD Shortcuts (ChoosingDialog)</br>
`R` --> `[LabVIEW Build-in]` `[Ctrl]` Remove And Rewire</br>
`S` --> `[Ctrl]` State Machine from Enum</br>
`T` --> `[LabVIEW Build-in]` `[Ctrl]` `[Shift]` Move Labels</br>
`U` -->  `[Ctrl]` `[Shift]` Cluster Auto-Sizing</br>
`V` --> _Reserved_</br>
`W` --> `[LabVIEW Build-in]` `[Ctrl]` `[Shift]` Wire Multiple Objects Together</br>
`X` --> _Reserved_</br>
`Y` --> _Reserved_</br>
`Z` --> _Reserved_</br>

## QD_NEVSTOP

### NEVSTOP QD Shortcuts(Choosing Dialog)

NEVSTOP Quickdrops. Using a choosing dialog for quick QD selection.

```
Default Shortcut - [Q]
```

### Control Operation

- `Reset Origin` : Resets the origin for all panes or the block diagram.
- `Hide Controls`/`Show Controls`
- `Enable Controls`/`Disble Controls`/`Disable&Grayout Controls`
- `Copy Boolean Caption to Boolean Text` : Copy selected boolean's caption to boolean text. If the booleans have no caption, label Text will be used instead.
- `Toggle Digital Increment Decrement Visible ( Swithc Show Or Hide ).vi`

### Clone Controls

This Quick Drop Keyboard Shortcut will clone the selected Control(s) or Indicator(s) on the Front Panel but changes Controls to Indicators and vice versa.  In addition, if found on the Connector Pane, it will attempt to place the newly created control on the opposite (left / right) side of the Connector Pane.

It was developed to automate the task where, for example,  you have a File Ref (in) control, and you want to wire it through the other side of the ConPane.

Note: This script only supports the following patterns: 4x2x2x4, 5x3x3x5, 6x4x4x6, and 8x6x6x8

### Erease Data(Clear Data)

Clear control/Constant's data. Clear Array QD is replaced. Supported type:
- Array
- String
- Listbox
- MulticolumnListBox
- Numeric
- Table
- Tree

```
Default Shortcut - [E]
```

### Refresh Palette

After some chane of Control/Function Pallette, you can manually update the pallette with this quickdrop.

### Smart Open VI Location in Explorer Window

Publish with sub-QuickDrop:
 - `Open Current VI's Location in Explorer Window`
 - `Open Selected VI's Location in Explorer Window`
 - `Open LabVIEW Program Folder`

When triggered on Front Panel:
Open Current VI's Location in Explorer Window.

When triggered on Block Diagram:
No SubVI is selected: Open Current VI's Location in Explorer Window.
SubVIs are selected: Open Selected VI's Location in Explorer Window.

```
Default Shortcut - [O]
```

### Align and Distribute

Align and Distribute slected controls/indicators/SubVIs. A pop-up dialog will be used for selecting the way you want.

```
Default Shortcut - [A]
```

### Cluster Auto-Sizing

Using a float dialog to choose cluster auto-sizing type. Press `Shift` to set the contained cluster items recursively.
- None
- Size to Fit
- Arrange Horizontally
- Arrange Vertically

```
Default Shortcut - [U]
Default Shortcut - [Shift][U]
```

### Build Array of References/Build Cluster of References

Create references with 'Build Array'/'buddle' together.

```
Default Shortcut - [B]
```

### Remove Unused Terminals on Nodes

Help users select Bundler nodes, Unbundler nodes and Property nodes to remove unused terminals.

Works for:
- Bundle By Name (Bundler > NamedBundler)
- Build Array (Bundler > BuildArray)
- Concatenate Strings (Bundler)
- Bundle (Bundler)
- Merge Errors (Bundler)
- Unbundle By Name (Unbundler > NamedUnbundler)
- Property Node (ObjectFunction > Property)

```
Default Shortcut - [Y]
```









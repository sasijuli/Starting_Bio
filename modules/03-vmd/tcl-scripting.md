# Tcl Scripting In VMD

## Goal

Understand that VMD can be controlled with Tcl commands.

## Why This Matters

Scripts make analysis reproducible. Instead of manually clicking through the same steps, you can save commands and run them again.

## Example

```tcl
mol new structure.pdb
mol representation NewCartoon
mol color Structure
mol addrep top
```

## Practice

- Find the VMD Tk Console.
- Run a simple command.
- Save useful commands in a notes file.

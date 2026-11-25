# MetaFactory 3.54.5 preview

## Change
The account table column header strip now uses matte charcoal (#292D33), soft-white text (#F2F4F7), subtle separators (#454A52), and a light-blue active sort label/arrow (#9BC7FF). Header height, column widths, account row stripes, checkboxes and interactions are preserved. This matches the approved dark-header preview.

No launch, selection, notes, reporting, EA, runtime, scheduling or update behavior changes in this release. All production source outside CopyGrid.cs is byte-identical to 3.54.4 except version declarations.

## Install
Close MetaFactory, then run MetaFactory-Setup-3.54.5-preview.exe.

## Verification
Built against Microsoft .NET Framework 4.5 reference assemblies. Existing English/Persian compact menu, selection, process-close, launch-stop, name/note interaction and Open/Show hover checks run at normal and simulated 125% scale. Header rendering screenshots were inspected. Installer PE/assembly versions, embedded app and native resources verified; package and remote installer hashes verified before delivery. No new broker/native execution validation is claimed for this color-only change.

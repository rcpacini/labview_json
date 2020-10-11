# labview_json
Lightweight JSON library for LabVIEW.

**No external dependencies, only 34 files, 851kB size**

## Features

* Full modification support to list, get, set, and pop elements
* Recursively create nested objects in a `{key:STR, type:U8ENUM, value:VARIANT}` type def.
* Pretty print indentation for JSON outputs.
* Enums can be exported as integers or strings.
* Float extensions support `Infinity`, `-Infinity`, `NaN`
* Timestamp support as ISO8601 offset date time strings `yyyy-mm-ddThh:mm:ss.uuuuuu+zz:zz`.
* Waveforms are objects with `{y0:TIMESTAMP, dt:DBL, Y:[DBL]}`.
* The `Root Path` parameter fetches nested elements by object keys or array indexes without needing to define the data structures.
* Use the `LVJSON Element.ctl` cluster to return complex structures recursively.
* __NO EXTERNAL DEPENDENCIES!!!__

## Supported Data Types

* Null (Empty Variant)
* Booleans
* Integers (I8, I16, I32, I64, U8, U16, U32, U64, U8ENUM, U16ENUM, U32ENUM)
* Floats (SGL, DBL, EXT)
* Strings (STR, PTH, TIMESTAMP, U8ENUM, U16ENUM, U32ENUM)
* Objects (CLUSTERS, WAVEFORMS, VARIANTS)
* Arrays (1D, 2D, nD...)

## API

* `JSON Unflatten.vi` - Unflattens JSON string to the LabVIEW Variant Data Type
* `JSON Flatten.vi` - Flattens LabVIEW Variant Data Type to JSON string
* `JSON Edit.vim` - Get, set or create LabVIEW Variant Data Types to/from JSON string

![LabVIEW JSON Library](docs/imgs/vi_tree.png)

## Examples

See the example VIs in the [json/examples](json/examples) directory.

![LabVIEW JSON Example](docs/imgs/example.png)

![LabVIEW JSON Example Modify](docs/imgs/example_modify.png)

## Unit Tests
Extensive unit testing

See the [json/tests](json/tests) directory.

To test, run `labview_json_tests.lvlib:test.vi`.

## YAJL (Yet Another JSON Library)
Yes, I understand there are a plethora of JSON libraries for LabVIEW
(Even built in ones).
Why this library, you ask? 
- Because LabVIEW's built in JSON libraries lack common operations other 
languages natively support (i.e. get, set, pop, list elements). 
- Because many libraries available are overly complicated with unnecessary class
abstraction and external dependencies. :(
- Because many libraries try to use magic data types to identify primitives
(i.e. Null) that only flummox basic usage.
- Because other libraries add maleware that require you to install crap all
over the place.

This a self contained JSON library for anyone that wants it. Period.

![LabVIEW JSON Library](docs/imgs/library.png)

Problems, create a ticket. Suggestions, create a ticket. Anything else, create a ticket.

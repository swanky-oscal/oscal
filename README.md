# Rust support for OSCAL

## oscal
Top level make file for cargo-make.  Start here.

There are cargo-make tasks for pulling the FedRAMP schema, and test data.

## Cargo-make
This repo uses cargo-make to simlify fetching dependent repos.  But it
is not necessary for simply building the libs, etc.

## OSCAL Schema
The code generator, for generating oscal_lib, requires the complete schema.  This will be automatically fetched by cargo-make.  The current version is v1.1.2.  If you just want to fetch the schema, run:

````bash
cargo make fetch-schema
````

## Building the artifacts

### oscal_types
This lib provide standard OSCAL data type, such as StringDatatype.  This is a dependency of oscal_lib and oscal_codegen.

### oscal_codegen
Generates Rust code from the full schema.  See the oscal_codegen README.md for details.

### oscal_lib
The main oscal lib.  The code for this lib was generated with [codegen](../oscal_codegen)

## OSCAL Documentation
- [NIST OSCAL on GitHub](https://github.com/usnistgov/OSCAL)
- [NIST OSCAL Reference](https://pages.nist.gov/OSCAL-Reference/models/)
- [GSA FedRAMP Automation](https://github.com/GSA/fedramp-automation)


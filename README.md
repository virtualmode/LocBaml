LocBaml
=======

LocBaml .NET implementation.

The LocBaml tool is not a production-ready application. It is presented as a sample that uses some of the localization APIs and illustrates how you might write a localization tool.

Publish
-------

To build release:

    dotnet publish -c Release

Usage
-----

1. Copy `LocBaml.exe` to your application's `bin\debug` folder, where the main application assembly was created.
2. To parse the satellite assembly file and store the output as a `.csv` file, use the following command:

    ./LocBaml.exe -parse HelloApp.resources.dll -out:HelloApp.resources_fr.csv

3. When you run `LocBaml` to parse files, the output consists of seven fields delimited by commas (`.csv` files) or tabs (`.txt` files).
4. Use the following syntax to generate a new `HelloApp.resources.dll` file. Mark the culture as `en-US`:

    ./LocBaml.exe -generate HelloApp.resources.dll -trans:HelloApp.resources_en.csv -cul:en -out:en

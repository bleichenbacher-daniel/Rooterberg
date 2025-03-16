# Tables

The directory Rooterberg/tables contains tables with test results and statistics. Each table is formatted with JSON and YAML.
This is done for convenience and readability. Corresponding files contain the same information. All tables are auto generated
from the source code and test results. The tables are updated with each release.

The following tables are available:
* **all_sets**: This table contains a list of the test vectors sorted by file name, as well as the test results obtained against
                various libraries. Libraries with failing tests are excluded.
* **libraries**: This table contains a list of test results sorted by language and library.
* **references**: This table contains a list of references.
* **index**: This table contains an inverted index from references to test vector sets that use a given reference.
 
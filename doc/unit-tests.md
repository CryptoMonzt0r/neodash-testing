Compiling/running unit tests
------------------------------------

Unit tests will be automatically compiled if dependencies were met in `./configure`
and tests weren't explicitly disabled.

After configuring, they can be run with `make check`.

To run the neodashd tests manually, launch `src/test/test_neodash`.

To add more neodashd tests, add `BOOST_AUTO_TEST_CASE` functions to the existing
.cpp files in the `test/` directory or add new .cpp files that
implement new BOOST_AUTO_TEST_SUITE sections.

To run the neodash-qt tests manually, launch `src/qt/test/test_neodash-qt`

To add more neodash-qt tests, add them to the `src/qt/test/` directory and
the `src/qt/test/test_main.cpp` file.

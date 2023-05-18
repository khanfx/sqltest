# MySQL Stored Procedure Unit Testing Framework
This framework provides a simple way to unit test MySQL stored procedures. It uses the Python unittest module to execute the stored procedures and assert the results.

Installation
To install the framework, run the following command:

pip install mysql-stored-procedure-unit-testing-framework

Code snippet

## Usage

To use the framework, create a new Python file and import the framework:

import mysql_stored_procedure_unit_testing_framework

Code snippet

Then, create a new test class that inherits from the framework's base class:

class MyTest(mysql_stored_procedure_unit_testing_framework.BaseTest):

In the test class, define the stored procedures that you want to test. You can do this by using the framework's @test_stored_procedure decorator:

@mysql_stored_procedure_unit_testing_framework.test_stored_procedure def test_my_stored_procedure():

Inside the test function, you can assert the results of the stored procedure. For example, you can assert that the stored procedure returns a specific value:

assert test_my_stored_procedure() == 1

Code snippet

You can also assert that the stored procedure raises an exception:

with pytest.raises(Exception): test_my_stored_procedure()

Code snippet

## Running the Tests

To run the tests, use the following command:

python -m unittest discover -s tests

Code snippet

This will run all of the tests in the `tests` directory.

## Example

Here is an example of a test class that tests a MySQL stored procedure:

class MyTest(mysql_stored_procedure_unit_testing_framework.BaseTest):

@mysql_stored_procedure_unit_testing_framework.test_stored_procedure def test_my_stored_procedure(self): """Test the my_stored_procedure stored procedure."""

Code snippet
# Assert that the stored procedure returns 1.
self.assertEqual(test_my_stored_procedure(), 1)
@mysql_stored_procedure_unit_testing_framework.test_stored_procedure def test_my_stored_procedure_raises_exception(self): """Test that the my_stored_procedure stored procedure raises an exception."""

Code snippet
# Assert that the stored procedure raises an exception.
with pytest.raises(Exception):
  test_my_stored_procedure()
Code snippet

To run this test class, use the following command:

python -m unittest discover -s tests

This will run the two tests in the tests directory. The first test will pass, and the second test will fail.

I hope this helps! Let me know if you have any other questions.

# DeveloperNotes-Python-UnitTesting
### To get Understanding og Unit testing in python
[Reference](https://docs.python.org/3/library/unittest.html#module-unittest)
[Source Code for Module unittest](https://pythonhosted.org/gchecky/unittest-pysrc.html)
____
1. The unittest unit testing framework
2. test fixture
   * A test fixture represents the preparation needed to perform one or more tests, and any associated cleanup actions
3. test case
    * A test case is the individual unit of testing. It checks for a specific response to a particular set of inputs. unittest provides a base class, TestCase,           which    may be used to create new test cases.
4. test suite
    * A test suite is a collection of test cases, test suites, or both. It is used to aggregate tests that should be executed together.
    
5. test runner
    * A test runner is a component which orchestrates the execution of tests and provides the outcome to the user. The runner may use a graphical interface, a            textual      interface, or return a special value to indicate the results of executing the tests.
    
_______
## Basic example
The unittest module provides a rich set of tools for constructing and running tests. This section demonstrates that a small subset of the tools suffice to meet the needs of most users..

Here is a short script to test three string methods:
```
import unittest

class TestStringMethods(unittest.TestCase):

    def test_upper(self):
        self.assertEqual('foo'.upper(), 'FOO')

    def test_isupper(self):
        self.assertTrue('FOO'.isupper())
        self.assertFalse('Foo'.isupper())

    def test_split(self):
        s = 'hello world'
        self.assertEqual(s.split(), ['hello', 'world'])
        # check that s.split fails when the separator is not a string
        with self.assertRaises(TypeError):
            s.split(2)

if __name__ == '__main__':
    unittest.main()
```
1. all my test cases running because of the call to `unittest.main()`.
2. inheriting from `unittest.TestCase` for every test class

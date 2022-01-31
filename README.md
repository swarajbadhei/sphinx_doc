# sphinx_doc
Steps to regenerate the github issue #10138.

1. naviagte into `./sphinx_doc/documentation/`.

2. run the command `sphinx-apidoc -f -o ./source/ ../python_dir/python_module_dir/`.(This directory contains the python files for which I want to generate rst files).

3. Above command will generate the following files.
  I. ./source/python_module_dir.rst (name of the dir where python files are kept)
  II. ./source/modules.rst

4. This should create rst files for the python files present inside `/python_dir/python_module_dir/`.

5. Now please remove the `__init__.py` file inside `/python_dir/python_module_dir/`.

6. execute `STEP-2` again.

7. This will generate the follwing files, just the way it should.
  I. ./source/python_functions.rst
  II. ./source/modules.rst

The problem here is : if the `__init__.py` is present, sphinx is not picking up the .py files present there. Need a way to solve it.

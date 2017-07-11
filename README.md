# numpy_wrapped_python_package
Python package with one dependency, the numpy package.  Note, this is not a build-dependency.  This project was created as a minimal example of introducing a third party python package with C-extensions as a dependency for your package.  While many examples exist, they all seem to strike the same middle-ground between minimal and exhaustive.  This is minimal.

To install:

- pip install -e git+https://github.com/jlimahaverford/numpy_wrapped_python_package.git#egg=requests_wrapped_python_package

```
Jonathan-Lima-MacBook-Pro:dist jonathanlima$ mkvirtualenv --python=/usr/local/bin/python3.6 test_env
    
    Running virtualenv with interpreter /usr/local/bin/python3.6
    Using base prefix '/usr/local/Cellar/python3/3.6.1/Frameworks/Python.framework/Versions/3.6'
    New python executable in /Users/jonathanlima/PythonEnvs/test_env/bin/python3.6
    Also creating executable in /Users/jonathanlima/PythonEnvs/test_env/bin/python
    Installing setuptools, pip, wheel...done.
    virtualenvwrapper.user_scripts creating /Users/jonathanlima/PythonEnvs/test_env/bin/predeactivate
    virtualenvwrapper.user_scripts creating /Users/jonathanlima/PythonEnvs/test_env/bin/postdeactivate
    virtualenvwrapper.user_scripts creating /Users/jonathanlima/PythonEnvs/test_env/bin/preactivate
    virtualenvwrapper.user_scripts creating /Users/jonathanlima/PythonEnvs/test_env/bin/postactivate
    virtualenvwrapper.user_scripts creating /Users/jonathanlima/PythonEnvs/test_env/bin/get_env_details
    
(test_env) Jonathan-Lima-MacBook-Pro:dist jonathanlima$ pip install -e git+https://github.com/jlimahaverford/numpy_wrapped_python_package.git#egg=requests_wrapped_python_package

    Obtaining requests_wrapped_python_package from git+https://github.com/jlimahaverford/numpy_wrapped_python_package.git#egg=requests_wrapped_python_package
      Cloning https://github.com/jlimahaverford/numpy_wrapped_python_package.git to /Users/jonathanlima/PythonEnvs/test_env/src/requests-wrapped-python-package
      Running setup.py (path:/Users/jonathanlima/PythonEnvs/test_env/src/requests-wrapped-python-package/setup.py) egg_info for package requests-wrapped-python-package produced metadata for project name numpy-wrapped-python-package. Fix your #egg=requests-wrapped-python-package fragments.
    Collecting numpy (from numpy-wrapped-python-package)
      Using cached numpy-1.13.1-cp36-cp36m-macosx_10_6_intel.macosx_10_9_intel.macosx_10_9_x86_64.macosx_10_10_intel.macosx_10_10_x86_64.whl
    Installing collected packages: numpy, numpy-wrapped-python-package
      Running setup.py develop for numpy-wrapped-python-package
    Successfully installed numpy-1.13.1 numpy-wrapped-python-package
    
(test_env) Jonathan-Lima-MacBook-Pro:dist jonathanlima$ pip freeze

    numpy==1.13.1
    -e git+https://github.com/jlimahaverford/numpy_wrapped_python_package.git@1b6ee14e11a276315a5cd1a2c9b84c9136fc1969#egg=numpy_wrapped_python_package
    pyspark==2.1.1+hadoop2.7
    (test_env) Jonathan-Lima-MacBook-Pro:dist jonathanlima$ python
    Python 3.6.1 (default, Apr  4 2017, 09:40:21) 
    [GCC 4.2.1 Compatible Apple LLVM 8.1.0 (clang-802.0.38)] on darwin
    Type "help", "copyright", "credits" or "license" for more information.
    
    >>> from numpy_wrapped_python_package import numpy_wrapped
    >>> numpy_wrapped.log(1)
    0.0
```


```
Jonathan-Lima-MacBook-Pro:dist jonathanlima$ mkvirtualenv --python=/usr/local/bin/python3.6 test_env

    Running virtualenv with interpreter /usr/local/bin/python3.6
    Using base prefix '/usr/local/Cellar/python3/3.6.1/Frameworks/Python.framework/Versions/3.6'
    New python executable in /Users/jonathanlima/PythonEnvs/test_env/bin/python3.6
    Also creating executable in /Users/jonathanlima/PythonEnvs/test_env/bin/python
    Installing setuptools, pip, wheel...done.
    virtualenvwrapper.user_scripts creating /Users/jonathanlima/PythonEnvs/test_env/bin/predeactivate
    virtualenvwrapper.user_scripts creating /Users/jonathanlima/PythonEnvs/test_env/bin/postdeactivate
    virtualenvwrapper.user_scripts creating /Users/jonathanlima/PythonEnvs/test_env/bin/preactivate
    virtualenvwrapper.user_scripts creating /Users/jonathanlima/PythonEnvs/test_env/bin/postactivate
    virtualenvwrapper.user_scripts creating /Users/jonathanlima/PythonEnvs/test_env/bin/get_env_details

(test_env) Jonathan-Lima-MacBook-Pro:dist jonathanlima$ pip install numpy

    Collecting numpy
      Using cached numpy-1.13.1-cp36-cp36m-macosx_10_6_intel.macosx_10_9_intel.macosx_10_9_x86_64.macosx_10_10_intel.macosx_10_10_x86_64.whl
    Installing collected packages: numpy
    Successfully installed numpy-1.13.1

(test_env) Jonathan-Lima-MacBook-Pro:dist jonathanlima$ pip install -e git+https://github.com/jlimahaverford/numpy_wrapped_python_package.git#egg=requests_wrapped_python_package

    Obtaining requests_wrapped_python_package from git+https://github.com/jlimahaverford/numpy_wrapped_python_package.git#egg=requests_wrapped_python_package
      Cloning https://github.com/jlimahaverford/numpy_wrapped_python_package.git to /Users/jonathanlima/PythonEnvs/test_env/src/requests-wrapped-python-package
      Running setup.py (path:/Users/jonathanlima/PythonEnvs/test_env/src/requests-wrapped-python-package/setup.py) egg_info for package requests-wrapped-python-package produced metadata for project name numpy-wrapped-python-package. Fix your #egg=requests-wrapped-python-package fragments.
    Requirement already satisfied: numpy in /Users/jonathanlima/PythonEnvs/test_env/lib/python3.6/site-packages (from numpy-wrapped-python-package)
    Installing collected packages: numpy-wrapped-python-package
      Running setup.py develop for numpy-wrapped-python-package
    Successfully installed numpy-wrapped-python-package

(test_env) Jonathan-Lima-MacBook-Pro:dist jonathanlima$ pip freeze

    numpy==1.13.1
    -e git+https://github.com/jlimahaverford/numpy_wrapped_python_package.git@1b6ee14e11a276315a5cd1a2c9b84c9136fc1969#egg=numpy_wrapped_python_package

(test_env) Jonathan-Lima-MacBook-Pro:dist jonathanlima$ python

    Python 3.6.1 (default, Apr  4 2017, 09:40:21) 
    [GCC 4.2.1 Compatible Apple LLVM 8.1.0 (clang-802.0.38)] on darwin
    Type "help", "copyright", "credits" or "license" for more information.
    
    >>> from numpy_wrapped_python_package import numpy_wrapped
    >>> numpy_wrapped.log(1)
    0.0
```
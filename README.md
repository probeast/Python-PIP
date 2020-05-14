# Python-PIP
Installation
Do I need to install pip?

pip is already installed if you are using Python 2 >=2.7.9 or Python 3 >=3.4 downloaded from python.org or if you are working in a Virtual Environment created by virtualenv or pyvenv. Just make sure to upgrade pip.
Installing with get-pip.py

To install pip, securely 1 download get-pip.py by following this link: get-pip.py. Alternatively, use curl:

curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py

Then run the following command in the folder where you have downloaded get-pip.py:

python get-pip.py

Warning

Be cautious if you are using a Python install that is managed by your operating system or another package manager. get-pip.py does not coordinate with those tools, and may leave your system in an inconsistent state.

get-pip.py also installs setuptools 2 and wheel if they are not already. setuptools is required to install source distributions. Both are required in order to build a Wheel Cache (which improves installation speed), although neither are required to install pre-built wheels.

Note

The get-pip.py script is supported on the same python version as pip. For the now unsupported Python 2.6, alternate script is available here.
get-pip.py options

--no-setuptools

    If set, do not attempt to install setuptools

--no-wheel

    If set, do not attempt to install wheel

get-pip.py allows pip install options and the general options. Below are some examples:

Install from local copies of pip and setuptools:

python get-pip.py --no-index --find-links=/local/copies

Install to the user site 3:

python get-pip.py --user

Install behind a proxy:

python get-pip.py --proxy="http://[user:passwd@]proxy.server:port"

get-pip.py can also be used to install a specified combination of pip, setuptools, and wheel using the same requirements syntax as pip:

python get-pip.py pip==9.0.2 wheel==0.30.0 setuptools==28.8.0

Using Linux Package Managers

See Installing pip/setuptools/wheel with Linux Package Managers in the Python Packaging User Guide.
Upgrading pip

On Linux or macOS:

pip install -U pip

On Windows 4:

python -m pip install -U pip

Python and OS Compatibility

pip works with CPython versions 2.7, 3.5, 3.6, 3.7, 3.8 and also PyPy.

This means pip works on the latest patch version of each of these minor versions. Previous patch versions are supported on a best effort approach.

pip works on Unix/Linux, macOS, and Windows.

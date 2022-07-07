# `pip` and `pipx`

- `pip`: libraries and applications
- `pipx`: applications

## Install Packages

### From PyPI (Default)

PyPI: Python Package Index

```bash
pip install <pkg-name> ...
```

or

```bash
python -m pip install <pkg-name> ...
```

### From GitHub

```bash
pip install git+<https://github.com/pypa/<pkg-name>.git@main>
```

### From .tar.gz

```bash
pip install <pkg-name>.tar.gz
```

### From wheel (.whl) Files

```bash
pip install <pkg.name>-<version>-py3-none-any.whl
```

### From requirements.txt Files

Use **`-r`**/**`--requirement`** option:

```bash
pip install -r requirements.txt
```

### Install "extra"

```bash
pip install <pkg>[<extra-name>]
```

For example:

```bash
pip install requests[security]
```

## Upgrade Pckages

Use option **`-U`**/**`--upgrade`**:

```bash
pip install --upgrade <pkg-name> ...
```

## Requirement Specifier

```plaintext
# <pkg-name><verion-specifier>
pip=22.1.0
```

```bash
pip install -U 'pip>=22.0'
```

[PEP 440](https://peps.python.org/pep-0440/ "Version Identification and Dependency Specification")
and [PEP 508](https://peps.python.org/pep-0508/ "Dependency specification for Python Software Packages")
contain a full specification of the specifiers that Python packaging currently supports.

### Version Specifier

The version component of a *Requirement Specifier*.

```plaintext
0.0.1           # latest version
==0.0.1         # specific version
>=0.0.1         # minimum version
~=0.1           # >=0.1,<0.2，equals to 0.1.x
>=0.0.1,<0.1.0
```

## Choose Download Source (Mirror)

Use option **`-i`**/**`--index-url`**:

```bash
pip install -i https://pypi.tuna.tsinghua.edu.cn/simple <pkg-name> ...
```

- <https://pypi.tuna.tsinghua.edu.cn/simple>
- <https://mirrors.aliyun.com/pypi/simple/>

## Using a Proxy Server

Use option **`--proxy`**:

```bash
pip install --proxy http(s)://<ip_or_host>:<port> <pkg-name> ...
```

## Uninstall Packages

```bash
pip uninstall <pkg-name>
```

## List Packages

```bash
pip list
pip list --outdated
```

## Show Details About Packages

```bash
pip show <pkg-name>
```

## Search Packages

```bash
pip search <pkg-name>
```

## Common Options

- **`--default-timeout`**: Set the default timeout in seconds.
- **`--timeout`**: Set the socket timeout, in seconds (default *`15`* seconds).
- **`--retries`**: Maximum number of retries each connection should attempt (default *`5`* times).

## `pipx`

### Set Up

```bash
pip install pipx

pipx ensurepath
pipx completions
```

### Usage

#### Install packages

```bash
pipx install <pkg> ...
```

#### List applications installed

```bash
pipx list
```

#### Uninstall applicaitons

```bash
pix uninstall <app> ...
```

## Install `pip`

```bash
python -m ensurepip --upgrade
```

## References

- [`pip` Documentation](https://pip.pypa.io/en/stable/)
- [`pipx` Documentation](https://pypa.github.io/pipx/)
- [PyPI Home](https://pypi.org)
- [PEP 440 - Version Identification and Dependency Specification](https://peps.python.org/pep-0440/)
- [PEP 508 - Dependency specification for Python Software Packages](https://peps.python.org/pep-0508/)
- [PEP 453 - Explicit bootstrapping of pip in Python installations](https://www.python.org/dev/peps/pep-0453)
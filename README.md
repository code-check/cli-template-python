# CLI App Template for Python

This is a template for creating CLI applications in Python.

You can build your console application in [app/app.py](app/app.py)

This template uses the `argparse` module. (For details see the [official documentation](https://docs.python.org/2.7/library/argparse.html).)

## Recieving Inputs
In [app.py](app/app.py) is a function called `main`:

``` python
def main(args, options):
```

All input arguments are passed into `args` as an array.  
If you want to use optional arguments, add them using `argparse`'s `parser.add_argument` in [cli.py](cli.py)

## Outputting Results
Use the standard `print()` method to output results to stdout.

``` python
  print(result)
```

## Installing External Libraries
If you want to use external libraries, do the following:

- Write the library name and version in [requirements.txt](requirements.txt)
- Add the following to [codecheck.yml](codecheck.yml):

``` yaml
build:
  - pip install -r requirements.txt
```

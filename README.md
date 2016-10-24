# Command line application template for Python2.x

Implement CLI application by editing [app.go](app.go).  
You may add new files to keep your code clean, if it is allowed in your challenge.

## How to get input parameters

In [app/app.py](app/app.py) is a function called `main`.
Build your console application there.  

``` python
def main(args, options):
  for arg in args:
    # Replace below line with your code.
    result = arg
```

All `stdin` input arguments are passed into `args` as an array.  

If you want to use optional arguments, add them using `argparse`'s `parser.add_argument` in [cli.py](cli.py)

## How to output result
You can use the standard `print()` method to output results to `stdout`.

``` python
print(result)
```

## Install External Libraries
If you want to use external libraries, do the following:

- Write the library name and version in [requirements.txt](requirements.txt)
- Add the following to [codecheck.yml](codecheck.yml):

``` yaml
build:
  - pip install -r requirements.txt
```

# CLI template for Python

This is template app for CLI test.  
You can make console application by editing [app/app.py](app/app.py)

This uses argparse module.. See detail in [argparse document](https://docs.python.org/2.7/library/argparse.html).

## How to get input parameters
app.py has a function `main`

``` ruby
def main(args, options):

```

All parameters are passed as `args` array

If you want to use option parameter, you can use `parser.add_argument` for your own option in [cli.py](cli.py)

## How to output result
You can use `print` method

``` python
  print(v)
```

## How to install external libraries
If you want to use external libraries, please do following

- Write library name and version in requirements.txt
- Add following section to codecheck.yml

``` yaml
build:
  - pip install -r requirements.txt
```

# exception

Extract unique Python-Exceptions with their traceback from a log file.

## WARNING!

The extraction logic here is heuristic and may fail you. Don't depend on it for any life or death situations. Also, please submit feedback on how it could be improved!

## Installational

Clone this repository and install with

```
python setup.py install
```

This adds a utility called `exception` or `exception.exe` to your path.

## Usage

To extract the Python tracebacks from a log called `logfile.txt`, run:

```
$ exception -f logfile.txt
```

If you want to exclude certain exceptions, try:

```
$ exception -f logfile.txt -e ValueError,AttributeError
```

You can all pass multiple filenames:

```
$ exception -f logfile1.txt logfile2.txt
```

This would exclude would exclude any `ValueError` or `AttributeError` tracebacks from the output.

The tool can also read the log file from stdout, e.g.:

```
cat logfile.txt | exception
```

or

```
cat logfile.txt | exception -e ValueError
```


Credits
---------

This is based on [a script](https://gist.github.com/originell/1923003) by [@originell](https://github.com/originell).

This package was created with Cookiecutter_ and the `audreyr/cookiecutter-pypackage`_ project template.

# nl-contact-tracing-odds-and-ends static html

![CI](https://github.com/minvws/nl-contact-tracing-odds-and-ends/workflows/CI/badge.svg)

## Static html
The output of scripts can be converted to (a) static html (page).

### Setup
In order to run, test or develop the static html generation.

Optionally, but strongly recommended, create a virtual environment for Python and Flask:
```

$ cd static/
$ virtualenv venv
$ source venv/bin/activate

```

Install Python dependencies:
```

$ pip3 install -r requirements.txt

```

Run a local webserver on port 5000, during development and/or testing of scripts/tools:
```

$ python3 serve.py 
  [...]
  * Running on http://127.0.0.1:5000/ (Press CTRL+C to quit)
  [...]

```

An example shell script is provided that runs one or more test scripts (phase 1), collects output (phase 2), start/stop local webserver (phase 3) to generate local html.

```

$  ./run.sh
NFO: generating static html
INFO: phase 1 = run test script(s)
INFO: phase 2 = collect output
INFO: phase 3 = generate static html
127.0.0.1 - - [10/Aug/2020 05:42:11] "GET / HTTP/1.1" 200 -
INFO: static html ok
INFO: kill python process (309617) ok
```

The resulting local html file will be placed in dir 'static_out/'). This output file can be used to place on public webserver (minus the css and img dirs).


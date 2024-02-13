# Derace

Derace is a Python package for debugging Python traces. It provides decorators for debugging the function by calling it with the `pdb` debugger attached. It also provides a main logic for debugging a trace.

## Installation

You can install the package using `pip`:

```bash
pip install derace
```

## Usage

The project consists of decorators for debugging and a main logic for debugging a trace. You can use them in your Python scripts as follows:

```python
from derace import debug

@debug
def your function():
    a = 1
    b = 0
    c = a / b
    return c

your_function()
```

output:
```cmd
Exception occurred in /home/hadi/work/derace/tests/test_debug_trace.py at line 8
Function `your_function`: 
        line c = a / b
Exception type: ZeroDivisionError
Exception message: division by zero
Stack trace:
> /home/hadi/work/derace/tests/test_debug_trace.py(8)your_function()
-> c = a / b
(Pdb)
```

This can be handy when you are using Jupyter notebooks and you want to debug a function.


## Contributing

If you want to contribute to the project, feel free to make a pull request.

## License

This project is licensed under the MIT License.
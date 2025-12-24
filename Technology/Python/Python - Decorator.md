
```python
@start()
def generate (self):
...
```

The code above is equivalent to this one:

```python
def generate(self):
...

generate = start(generate)
```

* start is called first

A decorator is a function that:
* Takes another function as input.
* Adds behaviour before and/or after it.
* Returns a new function.

This lets you **wrap** functionality without changing the original function’s code.

```python
@listen(generate_city)
def generate_fun_fact(self, random_city):
    ...
```

So:

1. `listen(generate_city)` is executed **at import time**
2. It receives `generate_city` as an argument
3. It returns a decorator
4. That decorator receives `generate_fun_fact`
5. The function is **registered as a listener** for `generate_city`

```python
generate_fun_fact = listen(generate_city)(generate_fun_fact)
```

* `kickoff()` method returns the the output from the last method called.
* `plot()` method will generate a HTML file, to help to understand the flow.
* flow.state will store the whole state from all the runs from a give flow that was executed.

#tech #python
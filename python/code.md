# Python code guidelines

* Use `uv venv` to use the project-level .venv environment when running python or python based tools.
* Use always type annotations. When interfacing external packages with no types, use `# type: ignore` comments, being as specific as possible.
* If the code deals with pytorch, jax, or other neural network package, use sync interfaces. Otherwise, try to provide async interfaces if the code needs to use IO, network or similar operations that can be used asynchronously.
* Always try to find libraries that can perform the work at hand, giving preference to python standard libraries and more mature libraries. Note up to 3 possible alternatives if necessary.
# operations-research-ortools

Exercises from my university Operations Research course, solved in Jupyter notebooks with
[Google OR-Tools](https://developers.google.com/optimization): linear and integer programming.

**Status:** coursework (2021)

## Why I built it

I wrote these to practice turning word problems into models and checking the answer with a
solver instead of by hand. The notebooks are in Portuguese.

## Quick start

```sh
cd listas/lista01
uv run --with ortools --with numpy --with jupyter jupyter lab q01.ipynb
```

To run a notebook headless instead, swap `jupyter lab q01.ipynb` for
`jupyter nbconvert --to notebook --execute q01.ipynb`. Both notebooks ran cleanly this way.

## What's in it

- `listas/lista01/q01.ipynb`: the diet problem, a linear program solved with GLOP
- `listas/lista01/q02.ipynb`: a production mix (toy soldiers and trains), an integer program solved with SCIP
- `listas/lista01/template.ipynb`: the small model I started each exercise from

Sample results, as saved in the notebooks:

| Notebook | Result |
| --- | --- |
| `q01` | minimum cost 4.04, buying 3.29 of beans, 5.1 of sugar and 8.55 of lettuce |
| `q02` | maximum profit 180, making 20 soldiers and 60 trains |

The course slides and exercise sheets aren't included; they belong to the course.

## How it works

Each notebook creates a solver, declares the variables, adds the constraints one by one with
the original inequality in a comment, sets the objective and prints the solution.

## License

MIT, see [LICENSE](LICENSE).

# mis_apuntes_isc

Study notes (in Spanish) for Computer Systems Engineering: Git/GitHub and
Machine Learning fundamentals, from linear regression to classification
with logistic regression. Every notebook runs end to end with the pinned
environment below.

## Setup

Requirements: Python 3.12 and a fresh clone (about 2 MB — the virtual
environment is intentionally **not** tracked in git).

```bash
git clone https://github.com/IanOlave0/mis_apuntes_isc.git
cd mis_apuntes_isc

python3 -m venv .venv
source .venv/bin/activate

pip install -r requirements.txt
python -m ipykernel install --user --name mis_apuntes_isc
```

Then open any notebook in `apuntes_ML/` with the `mis_apuntes_isc` kernel
and run all cells.

## Layout

- `apuntes_ML/` — ML labs: `01` intro, `02` linear regression,
  `03` gradient descent, `04` multiple regression, `05` gradient descent
  in practice (scaling, polynomial features), `06` classification with
  logistic regression.
- `apuntes_gitygithub/` — Git and GitHub notes.
- `requirements.txt` — pinned versions (NumPy, Matplotlib, ipykernel)
  that every notebook was verified against.

## Reproducibility

`requirements.txt` pins the exact versions all notebooks were executed
with. To verify from scratch: create a fresh virtualenv, install the
requirements, and execute every code cell of every notebook under
`apuntes_ML/` — all of them must run without errors.

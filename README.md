# mis_apuntes_isc

> [English](#setup) · [Versión en español](#versión-en-español)

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

---

## Versión en español

Apuntes de estudio (en español) para Ingeniería en Sistemas
Computacionales: Git/GitHub y fundamentos de Machine Learning, desde
regresión lineal hasta clasificación con regresión logística. Cada
notebook corre de principio a fin con el entorno fijado abajo.

## Instalación

Requisitos: Python 3.12 y un clon fresco (unos 2 MB — el entorno virtual
intencionalmente **no** está trackeado en git).

```bash
git clone https://github.com/IanOlave0/mis_apuntes_isc.git
cd mis_apuntes_isc

python3 -m venv .venv
source .venv/bin/activate

pip install -r requirements.txt
python -m ipykernel install --user --name mis_apuntes_isc
```

Luego abre cualquier notebook en `apuntes_ML/` con el kernel
`mis_apuntes_isc` y ejecuta todas las celdas.

## Estructura

- `apuntes_ML/` — labs de ML: `01` intro, `02` regresión lineal,
  `03` descenso del gradiente, `04` regresión múltiple, `05` descenso del
  gradiente en la práctica (escalamiento, features polinomiales),
  `06` clasificación con regresión logística.
- `apuntes_gitygithub/` — apuntes de Git y GitHub.
- `requirements.txt` — versiones fijadas (NumPy, Matplotlib, ipykernel)
  contra las que se verificó cada notebook.

## Reproducibilidad

`requirements.txt` fija las versiones exactas con las que se ejecutaron
todos los notebooks. Para verificar desde cero: crea un virtualenv
nuevo, instala los requirements y ejecuta cada celda de código de cada
notebook en `apuntes_ML/` — todas deben correr sin errores.

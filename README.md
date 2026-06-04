# GeoUNED Jupyter Visualization

Minimal notebook: load one STEP file, convert it with GeoUNED, and view generated cells in 3D.

## Install

Use a short folder path on Windows, for example `C:\gjv`.

```powershell
micromamba create -y -p .\.venv -f environment.yml
```

## Run

```powershell
$env:PYTHONNOUSERSITE = "1"
.\.venv\python.exe -m jupyter lab
```

Open `geouned_jupyter_visualization.ipynb`.

## Test

```powershell
$env:PYTHONNOUSERSITE = "1"
.\.venv\python.exe -m nbconvert --to notebook --execute --inplace .\geouned_jupyter_visualization.ipynb --ExecutePreprocessor.kernel_name=python3
```

To switch examples, edit the first notebook cell:

```python
examples = [Path("example_0.step"), Path("example_4.step")]
path = examples[0]
```

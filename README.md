# Manim experiments — starter

A Jupyter notebook introducing **2D linear transformations** with Manim Community Edition. Designed for a **GitHub Codespace** using the VS Code notebook editor.

## Setup in a Codespace (Ubuntu/Debian)

Open the Codespace terminal at the repository root and run:

```bash
sudo apt-get update
sudo apt-get install -y build-essential python3-dev pkg-config libcairo2-dev libpango1.0-dev ffmpeg
python3 -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
python -m ipykernel install --user --name manim-experiments --display-name "Python (manim-experiments)"
```

Open `01_linear_transformations.ipynb` in the Codespaces VS Code editor. Select **Python (manim-experiments)** in the notebook's kernel selector, and **Run All**.

Manim renders an MP4 and embeds the animation below the `%%manim` cell. First renders may take a little longer than subsequent ones. The video files are stored under `media/` (ignored by Git).

**Notes**
- If you're starting a new terminal, run `source .venv/bin/activate` to activate the environment again. The notebook kernel remembers the `.venv` Python interpreter independently of your terminal.
- The `%%manim` line must be **the first line** of its notebook code cell (no import statements, blank lines, or comments before it).
- The demo uses Manim's `Text`-free `LinearTransformationScene`; a full LaTeX installation is **not** required. If you later use `MathTex` or `Tex`, you'll need LaTeX packages.
- You may need to install/enable the Python and Jupyter extensions in Codespaces' VS Code environment.
- `requirements.txt` handles Python packages; the `apt-get` step handles Manim's native graphics/video dependencies.

## Contents

- `01_linear_transformations.ipynb`: inspect a matrix numerically; animate its transformation of the grid, basis vectors, unit square and a sample vector; animate the inverse.
- `requirements.txt`: Python dependencies.
- `.gitignore`: avoids committing the virtual environment and rendered media.

## First matrix

\[ A = \begin{bmatrix} 1 & -1 \\ -1 & 2 \end{bmatrix} \]

The columns tell you where the standard basis vectors land. Here, `det(A)=1`, so area is preserved, even though lengths and angles generally are not.

For further reading: [Manim installation](https://docs.manim.community/en/stable/installation.html), [Manim Jupyter documentation](https://docs.manim.community/en/stable/installation/jupyter.html), [LinearTransformationScene](https://docs.manim.community/en/stable/reference/manim.scene.vector_space_scene.LinearTransformationScene.html).

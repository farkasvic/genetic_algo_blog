# Survival of the Fittest (Model): Optimizing with Genetic Algorithms

A Quarto blog exploring bio-inspired optimization in machine learning. The main tutorial walks through building a **Genetic Algorithm** (GA) to evolve hyperparameters for a Random Forest classifier—demonstrating how concepts like crossover, mutation, and fitness selection can outperform traditional methods like GridSearch and RandomSearch.

## What's Inside

- **Main tutorial** (`index.qmd`): A step-by-step guide to implementing genetic algorithms for hyperparameter tuning, including:
  - Mapping biological concepts (individuals, chromosomes, genes) to ML models
  - Crossover, mutation, and fitness functions in Python
  - A comparison of GA vs. RandomizedSearchCV on the Digits dataset

- **Posts** (`posts/`): Additional blog posts and code examples

- **About** (`about.qmd`): Author and blog information

## Tech Stack

- [Quarto](https://quarto.org/) for the website
- Python (scikit-learn, matplotlib, numpy) for the tutorials

## Getting Started

1. **Install Quarto** (if needed): [quarto.org/docs/get-started](https://quarto.org/docs/get-started/)

2. **Set up Python environment** (for running the code in the tutorial):
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   pip install -r requirements.txt
   ```

3. **Render the site**:
   ```bash
   quarto render
   ```

4. **Preview locally**:
   ```bash
   quarto preview
   ```

The rendered site is output to `docs/`.

## Automatic Deployment (GitHub Actions)

The site is automatically built and published to **GitHub Pages** on every push to `main` or `master`.

**One-time setup** (in your GitHub repo):

1. Go to **Settings → Pages** and set the source to the `gh-pages` branch (root).
2. Go to **Settings → Actions → General** and under "Workflow permissions" select **Read and write permissions**.

After that, each commit will trigger a rebuild and redeploy. You can also run the workflow manually from the **Actions** tab.

## Project Structure

```
├── index.qmd          # Main blog page & GA tutorial
├── about.qmd          # About page
├── posts/             # Blog posts
├── _quarto.yml        # Quarto website config
├── styles.css         # Custom styles
├── requirements.txt   # Python dependencies
├── .github/workflows/ # GitHub Actions (auto-publish on push)
└── docs/              # Rendered output (local)
```

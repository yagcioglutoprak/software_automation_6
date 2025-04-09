# Exemple d'Automatisation de Build avec GitHub Actions

Ce projet démontre l'utilisation de GitHub Actions pour automatiser la vérification de la qualité du code Python.

## Configuration

1. Le fichier `main.py` contient un bug d'indentation intentionnel
2. Le workflow GitHub Actions vérifie automatiquement le code avec Black et Flake8
3. Le workflow est déclenché lors des pull requests vers la branche main

## Utilisation

### Installation locale des outils

```bash
pip install -r requirements.txt
```

### Exécution locale des vérifications

```bash
black --check .
flake8 .
```

### Workflow GitHub Actions

Le workflow est défini dans `.github/workflows/lint.yml` et s'exécute automatiquement lors des pull requests.

### Correction du bug

Pour corriger le bug d'indentation dans `main.py`:

```python
def hello_world():
    print("Hello, world!")  # Indentation correcte avec 4 espaces

hello_world()
``` 
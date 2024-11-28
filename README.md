# Docker Message Action

Cette action Docker génère et affiche un message personnalisé.

## Inputs

| Nom     | Description                | Obligatoire | Valeur par défaut |
|---------|----------------------------|-------------|--------------------|
| who-to-greet | Who to greet     | Oui         | -                  |

## Outputs

| Nom            | Description                |
|-----------------|----------------------------|
| output-message  | Le message généré par l'action |

## Exemple d'utilisation

```yaml
name: Exemple de workflow
on:
  push:
    branches:
      - main

jobs:
  message-job:
    runs-on: ubuntu-latest
    steps:
    - name: Checkout code
      uses: actions/checkout@v4

    - name: Exécuter l'action Docker
      uses: ./ # Utilise l'action locale
      with:
        who-to-greet: "Salut de l'action Composite"
```

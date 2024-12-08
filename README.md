# Diagramme Pieuvre

Une bibliothèque Python pour générer des diagrammes pieuvre (diagrammes des interacteurs) pour l'analyse fonctionnelle.

## Installation

```bash
pip install diagramme-pieuvre
```

## Utilisation

```python
from diagramme_pieuvre import DiagramPieuvre, create_diagram
from diagramme_pieuvre.examples import systeme_cafe

# Utilisation rapide avec un exemple
create_diagram(systeme_cafe)

# Ou création personnalisée
mon_systeme = {
    'name': "Mon Système",
    'text': "Description\ndu système",
    'color': '#90EE90',
    'elements': [
        ('elem1', 'FC1', 'Élément 1', '#FFE0E0', '#FF0000'),
        ('elem2', 'FC2', 'Élément 2', '#E0FFE0', '#00FF00')
    ],
    'fp_connections': [
        ('elem1', 'elem2', 'FP1', 'blue')
    ]
}

diagram = DiagramPieuvre(mon_systeme)
diagram.setup_diagram()
diagram.save_and_show("mon_diagramme.svg")
``

# Automation Python — Tutoriel

## Automatisez la préparation des publications de Mireille avec Python

**Durée :** 10 minutes · **Niveau :** débutant · **Prérequis :** Python 3

### Mise en situation

Mireille crée du contenu sur les nouvelles technologies. Chaque semaine, elle rassemble des sujets, prépare ses vidéos et rédige ses publications. Ces tâches répétitives lui prennent du temps : elle souhaite développer une petite application pour mieux les organiser.

Votre mission : créer un outil Python qui prépare son calendrier éditorial.

### 1. Décrivez une publication

Chaque publication possède un titre, une plateforme et un statut :

```python
publication = {
    "titre": "Comprendre les agents IA",
    "plateforme": "YouTube",
    "statut": "à valider"
}
```

### 2. Préparez le message de Mireille

```python
def preparer_message(publication):
    return (
        f"Mireille vous présente : {publication['titre']}.\n"
        "Quel sujet aimeriez-vous découvrir ensuite ?"
    )

print(preparer_message(publication))
```

Résultat :

```text
Mireille vous présente : Comprendre les agents IA.
Quel sujet aimeriez-vous découvrir ensuite ?
```

### 3. Ajoutez une validation

Mireille souhaite relire ses contenus avant leur publication. Votre application doit donc distinguer les contenus « à valider », « validés » et « publiés ».

```python
publications = [
    publication,
    {
        "titre": "Automatiser ses tâches avec Python",
        "plateforme": "Facebook",
        "statut": "validé"
    }
]

for contenu in publications:
    if contenu["statut"] == "validé":
        print(preparer_message(contenu))
```

Cette boucle prépare uniquement les messages validés. Elle ne publie rien sur les plateformes.

### À vous de jouer

1. Ajoutez une date de publication à chaque contenu.
2. Ajoutez une troisième publication pour Mireille.
3. Affichez le titre, la plateforme et la date des contenus validés.

---

*Scénario pédagogique fictif, inspiré du principe de préparation éditoriale d’Engineering Brief. Aucune publication réelle ni connexion à un compte social n’est effectuée.*

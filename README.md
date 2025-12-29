# Jeu de Poursuite

Un mini-jeu de survie en HTML/CSS/JavaScript où vous devez échapper à des monstres et les piéger.

## Comment jouer

| Contrôle | Action |
|----------|--------|
| Souris | Déplacer le personnage |
| Clic gauche | Poser un piège |

## Objectif

Survivre le plus longtemps possible en évitant les monstres qui vous poursuivent. Utilisez les pièges pour les éliminer.

## Éléments du jeu

| Élément | Icône | Description |
|---------|-------|-------------|
| Joueur | 😊 | Vous contrôlez ce personnage avec la souris |
| Monstre rapide | 👹 | Rouge, vitesse élevée (2.5) |
| Monstre lent | 👻 | Violet, vitesse modérée (2.0) |
| Piège | 🪤 | Élimine un monstre au contact |

## Système de pièges

- **Stock initial** : 3 pièges
- **Régénération** : +1 piège toutes les 5 secondes
- **Bonus** : +1 piège par monstre éliminé
- Les monstres réapparaissent 1.5s après leur mort

## Lancer le jeu

Ouvrir `index.html` dans un navigateur web.

## Structure du code

```
index.html
├── CSS (styles intégrés)
│   ├── Animations (pulse, explosion, mort)
│   └── Design néon/cyberpunk
└── JavaScript
    ├── Boucle de jeu (requestAnimationFrame)
    ├── Gestion des collisions
    ├── IA de poursuite des monstres
    └── Système de pièges
```

## Fonctions principales

| Fonction | Rôle |
|----------|------|
| `gameLoop()` | Boucle principale du jeu |
| `updateMonsters()` | Déplacement des monstres vers le joueur |
| `checkCollision()` | Détection collision joueur/monstre |
| `checkTrapCollisions()` | Détection collision monstre/piège |
| `placeTrap()` | Pose un piège à la position du clic |
| `killMonster()` | Gère la mort et le respawn d'un monstre |
| `restartGame()` | Réinitialise la partie |

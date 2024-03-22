# 17_alien_vs_predator_part_3

Alien vs Predator - Épisode 3

Objectif du Projet:
Développer un programme de vision par ordinateur capable de différencier de manière précise un Alien d'un Predator.

Contexte du Projet:
Dans l'épisode précédent, nous avons constaté que la technique de "data augmentation" est efficace pour réduire le surapprentissage, mais elle apporte peu d'amélioration (dans notre exemple !) à la performance de différenciation entre une image d'un Alien et une image d'un Predator. Dans cet épisode, nous allons utiliser la technique de "transfer learning", plus précisément l'extraction de caractéristiques ("features extraction"), pour améliorer les performances du programme de vision par ordinateur.

Procédure:

Charger le modèle VGG-16.
Extraire les caractéristiques des images des ensembles d'apprentissage, de validation et de test via VGG-16.
Entraîner un perceptron multi-couches avec le code Keras/TensorFlow suivant pour prédire la sortie (Alien ou Predator):
python
Copy code
model = models.Sequential()
model.add(layers.Dense(units=256, activation='relu', input_dim=4 * 4 * 512))
model.add(layers.Dense(units=1, activation='sigmoid'))
Conclusion:
La combinaison de l'extraction de caractéristiques par VGG-16 et l'utilisation d'un perceptron multi-couches avec la structure spécifiée a été adoptée pour améliorer la précision du programme de vision par ordinateur dans la distinction entre Aliens et Predators.

Tâches Optionnelles:
Pour les plus audacieux :

Tester d'autres modèles que VGG-16 pour l'extraction de caractéristiques.
Expérimenter avec d'autres modèles de Machine Learning, tels que SVM, pour la phase de supervision.
Livrables:
Des Jupyter Notebooks.

Critères de Performance:
Le code en langage Python doit être clair, bien commenté et facile à comprendre. La précision du modèle dans la distinction entre Aliens et Predators sera évaluée comme critère de performance.

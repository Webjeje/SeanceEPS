# Mode d’emploi – Générateur de séance EPS (A4 paysage)

 Objectif : produire rapidement une fiche **A4 paysage**, dense et imprimable, avec **vision globale** (Contexte + objectifs + tableau des situations), **stockage** des séances ou des situations récurrentes (JSON) et **schéma** d’organisation (dessin carré).

[![Watch the video](https://img.youtube.com/vi/af7hSFUDhdU/maxresdefault.jpg)](https://youtu.be/af7hSFUDhdU)

### [Lien Vidéo](https://youtu.be/af7hSFUDhdU)


# 1) Démarrage rapide (5 min)

1. Ouvrir la page et compléter l’**entête** (APSA, Classe, Champ d’apprentissage, Matériel, Date, Séance n°).
2. Renseigner les 3 zones : **Attendus**, **Objectif de séquence**, **Objectif de séance**.
3. Cliquer **« Ajouter une situation »** (bouton dans la barre ou sous le tableau).
4. Dans le **modal** :

   * **Section 1** : N°, Durée, Situation, Objectif, But.
   * **Section 2** : « Organisation / dispositif » (texte) + **schéma** (outil trait / rectangle / cercle / point, couleur, annuler, supprimer, effacer tout, adapter).

     * Astuce : passer en **mode Sélection** (curseur) pour déplacer/redimensionner/pivoter les éléments.
   * **Section 3** : Critère de réalisation / réussite, Variables (général, +, −).
5. Cliquer **Enregistrer** : la ligne est ajoutée (le **schéma** est inséré en **vignette carrée** dans la colonne « Organisation / dispositif »).
6. Répéter pour toutes les situations.
7. **Imprimer** (A4 paysage) ou **Exporter JSON** pour réutiliser ultérieurement.



# 2) Vue d’ensemble & principes de mise en page

* **Format** : A4 **paysage** ; page destinée à l’impression (marges réduites).
* **Densité** : interface **compacte** (polices et marges réduites) → **plus d’infos par page**.
* **Couleurs** (repères visuels) :

  * Entête : bleu clair
  * Attendus : jaune pâle
  * Obj. séquence : vert pâle
  * Obj. séance : orange pâle
  * Entêtes de tableau : bleu gris clair
* **Tableau des situations** :

  * Colonnes : N°, Durée, Situation, Objectif, **Organisation / dispositif**, But, Critère de réalisation, Critère de réussite, Variable, Actions.
  * **Organisation / dispositif** = **60%** de la largeur (écran **et** impression).
  * Les lignes impaires sont légèrement **alternées** (meilleure lisibilité).
* **Tri des situations** : affichage **trié par N°** (croissant) → pour réorganiser, **modifiez le N°**.



# 3) Barre d’outils (haut de page)

* **Ajouter une situation** : ouvre le modal d’édition.
* **Exporter JSON** : télécharge `seance-eps.json` (entête + toutes les situations + schémas).
* **Importer JSON** : charge un fichier JSON depuis votre ordinateur (**remplace** le contenu en cours).
* **Imprimer** : lance l’impression (éléments non pertinents masqués).

> Remarque : pas d’auto-sauvegarde. **Exporter** le JSON pour conserver votre travail avant de fermer la page.



# 4) Le modal « Ajouter / Modifier une situation »

## Section 1 – Items de cadrage

* **N°** (entier) : sert à l’**ordre** d’affichage.
* **Durée** : ex. `15’`.
* **Situation** : tâche, consignes, contraintes.
* **Objectif** : capacité visée (technique, tactique, expressive, énergétique…).
* **But (ancrage CA)** : CA1/CA2/CA3/CA4 (liste).

## Section 2 – Organisation & description (texte + schéma)

* **Texte** « Organisation / dispositif » : groupes, rotations, ateliers, matériel, traçage…
* **Schéma** (canvas **carré**) :

  * **Outils** :

    * Trait (slash), Rectangle, Cercle, Point (petit disque plein).
    * **Sélection** (curseur) : déplacer, **redimensionner**, **pivoter** les objets.
  * **Actions** :

    * **Annuler le dernier** (Undo).
    * **Supprimer l’objet sélectionné**.
    * **Effacer tout**.
    * **Adapter à la zone** (fit) : recalcul du canvas dans son conteneur.
  * **Couleur** : pipette pour changer la couleur des tracés/points **avant** de dessiner.
  * **Astuce de netteté** : à l’enregistrement, le schéma est exporté en PNG avec un facteur lié à l’**écran** (DPR) pour une vignette **nette** à l’impression.

### Raccourcis utiles (dans le canvas)

* **Suppr / Backspace** : supprime l’objet **sélectionné**.
* **Échap** : repasser rapidement en **outil « Trait »** (mode dessin).

> Important : la **vignette** 1:1 (ratio carré) est automatiquement **insérée** dans la colonne « Organisation / dispositif » quand vous cliquez **Enregistrer**.

## Section 3 – Critères & Variables

* **Critère de réalisation** : qualité d’exécution (alignements, rythme, enchaînement…).
* **Critère de réussite** : seuils/indicateurs (ex. 3/5, 20″ sans faute…).
* **Variables (général)** : distances, temps, nombre de joueurs, surface, règles…
* **Variables +** (complexification) : ex. + distance, − temps, + contraintes, + opposition.
* **Variables −** (allègement) : ex. − distance, + temps, − contraintes, − opposition.



# 5) Édition & suppression des situations

* **Modifier** (icône crayon) : réouvre le modal prérempli, y compris le **schéma** (chargé en mode éditable).
* **Supprimer** (icône poubelle) : confirmation → retire la ligne.
* **Réorganiser** : changer la valeur de **N°** (le tri est automatique à l’affichage).



# 6) Export / Import (JSON)

## Export

* Clique **Exporter JSON** → un fichier `seance-eps.json` est téléchargé.
* Contenu :

  * **entete** : apsa, classe, champ, matériel, date, séance, attendus, objectifSequence, objectifSeance.
  * **situations** : champs texte + **drawingJSON** (objets Fabric pour ré-édition) + **drawingDataUrl** (PNG vignette pour l’impression).

## Import

* Clique **Importer JSON** → choisir un fichier `.json`.
* Le contenu **remplace** la séance en cours (pensez à exporter avant si nécessaire).

> Conseils :
>
> * Versionnez vos fichiers : `seance-eps_2025-09-07_v1.json`.
> * Vous pouvez constituer une **bibliothèque** de situations/séances récurrentes et ne charger que ce qu’il faut selon les classes.

![Watch the video](https://www.webjeje.com/online/assets/seance.png)

# 7) Impression (A4 paysage)

* La page est optimisée pour l’impression :

  * **A4 paysage**, marges réduites (densité maximale).
  * **Masqués** : barre d’outils, boutons d’action, badges « outils », modals.
  * **Colonne « Organisation / dispositif » = 25%** assurée sur la version papier.
  * Styles de bordures adaptés pour une **lisibilité nette**.

> Astuce : si votre imprimante ajoute des marges, activez « **Ajuster à la page** » ou réduisez l’échelle (ex. 95 %).

---

# 8) Bonnes pratiques & astuces

* **Numérotez** vos situations en pensant à l’**ordre pédagogique** (le tri s’appuie sur ce N°).
* **Écrivez court** dans les cellules (la densification accroît la charge visuelle → phrases télégraphiques = plus lisible).
* Pour le **schéma** :

  * Utilisez **formes simples** + légende minimale ; inutile de trop détailler.
  * Passez en **mode Sélection** pour repositionner précisément.
  * « **Adapter** » si la zone a été redimensionnée.
* **Sauvegardez** : exportez le JSON **régulièrement** (pas d’auto-save).
* **Réemplois** : gardez une **banque** de JSON par APSA / niveau / objectifs (gain de temps énorme).
* **Impression** : faites un **aperçu** avant d’imprimer pour vérifier la pagination.



# 9) Limitations connues

* **Pas de sauvegarde automatique** (pas de LocalStorage) : fermeture/rafraîchissement = **perte** si vous n’avez pas exporté le JSON.
* L’import **remplace** la séance chargée (pas de fusion).
* Le module dessin est volontairement **minimal** (pas de texte, pas d’images importées).
* La densité élevée peut nécessiter une **police un peu plus grande** si la classe lit la fiche en autonomie (à ajuster si besoin).



# 10) Dépannage (FAQ)

**Q1. Mon schéma n’apparaît pas dans la colonne.**
→ Vérifiez que vous avez bien **ajouté au moins un objet** sur le canvas puis cliqué **Enregistrer**. Le PNG est généré automatiquement.

**Q2. Je ne peux pas déplacer un objet.**
→ Activez le **mode Sélection** (icône curseur). Les poignées apparaissent pour déplacer/redimensionner/pivoter.

**Q3. Le trait ne prend pas la couleur choisie.**
→ La couleur s’applique aux **nouveaux objets**. Changez la couleur **avant** de dessiner.

**Q4. Je voudrais revenir en arrière plusieurs fois.**
→ Le bouton **Annuler le dernier** supprime le dernier objet (répétez si besoin). Pas d’historique multi-niveaux.

**Q5. Après redimensionnement de la fenêtre, le canvas paraît décalé.**
→ Cliquez **Adapter à la zone** (ou rouvrez le modal) pour recalculer l’offset.

**Q6. Après import JSON, mes anciennes situations ont disparu.**
→ C’est normal : l’import **remplace** la séance. Exportez toujours votre travail avant d’importer un autre fichier.



# 11) Pistes d’évolution (si besoin)

* Option **épaisseur du trait** (+ gomme).
* **Duplication** d’objet au sein du canvas.
* **Quadrillage** de fond (repères de distances).
* **LocalStorage** (auto-sauvegarde) + **versionning** interne.
* **Slider de densité** (écran/impression) pour s’adapter aux usages de lecture.





# Login


Objectif :  Permet la connexion d'un utilisateur tout en conservant les données sur son avancement.

Résumé général: S'effectue lorsqu'un utilisateur ou un visiteur veux se connecter.

#Données :

Acteur Principal : Utilisateur

Acteurs secondaires : Admin

Fréquence   : fréquence de la connexion

Concurrence : Non

Déclencheur : se déclenche lors de la connexion de l'utilisateur, ou à la fin d'une inscription

## Pré-conditions :

### Données d'entrées :
	login

	mot de passe

Avoir un compte dans la base de donnée, pour cela il dois [s'inscrire](/inscription.md).
L'inscription dois être effectué préalablement.

## Post Conditions :

### Données sortie :
	TODO


En cas de succès : L'utilisateur a accès à son compte. Une session est créée, l'utilisateur est soit placé sur son Tableaudebord soit sur la dernière page ou il était.


En cas d'échec: affiche d'erreur mot de passe, actualisation de la page de connection.

# Navigation / IHM  :

Principe de navigation du scénario principal, organisation de l'IHM.

L'utilisateur ou le visiteur est sur la page de connexion sois en cliquant sur "Se connecter" dans la page d'acceuil sois en entrant directement l'URL, il entre ses informations et tente de se connecter si ses information sont valides il auras alors accés à son compte, dans le cas contraire un messages d'erreur apparait.

##Scénarios :

# MAIN SUCCESS SCENARIO

Step    Action

S    L'utilisateur est sur la page de connexion, il entre ces données et clique sur le bouton connexion.

1    Ce cas d'utilisation commence quand l'utilisateur clique sur le bouton "Se connecter" ou quand on entre l'url de connexion dans un navigateur.

2    On entre son login et son mot de passe.

3    On clique sur le bouton "Connexion".

4    Ce cas d'utilisation se fini lorsque l'utilisateur a accès à son compte après avoir cliqué sur "Connexion".

EXTENSION SCENARIOS

Step    Branching Condition

1	 Lorsque l'utilisateur s'est trompée dans ses informations. Etape 3 du scénario principale.

3	 Lorsque le visiteur n'as pas de compte. Etape 3 du scénario principale.

na.  Action causing branching:

1 : On propose à l'utilisateur d'entrer à nouveau ses informations et on affiche la mention [mot de passe oublié](/oublie.md).

2 : On propose au visiteur de [s'inscrire](/inscription.md).


# RELATED INFORMATION

Concurrency    Si un utilisateur tente de se connecter avec une autre instance on ferme la première.

Include Use Cases    [Inscription](/inscription.md)
 

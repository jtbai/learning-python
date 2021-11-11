# Les contrôles de flow
Les contrôlent de flow permettent de créer un chemin que le compilateur suivra afin d'arriver à la fin d'un script.
Ils créent *la logique applicative* ou encore le logiciel


```
  si quelque chose est vrai alors :
      fais ceci
  sinon:
      fait cela


  tant et aussi longtemps que ceci est vrai:
       fait cela


  pour tous les éléments de cette liste:
       fait cela
```



## Les 3 controles de flow 
Les 3 contrôles les plus fréquents


1. `if`: évalue une condition et exécute le code suivant si c'est vrai
   1. `else`: si l’if précédent est faux, évalue ce code à la place
   2. `elif`: combine `else` et `if` permettant d'appliquer une nouvelle condition si la précédente est fausse
2. `while`: évalue une condition et exécute une boucle de code tant que la condition n'est pas invalidée
1. `for ... in`: exécute une boucle de code pour chacun des éléments d'un `iterable`
   1. `break`: dans une boucle for on peut sortir en tout temps grâce à cet opérateur


### iterable
Un iterable est une variable qui contient plusieurs éléments sur lesquels on peut obtenir séquentiellement le prochain élément


### les `:` 
Dans `python`, pour terminer une instruction de contrôle de flow, on utilise les `:`. Après ce symbole on écrit le code à exécuter.


```
si ceci:
   alors fais cela
```



### indentation
Dans `python`, le code est indenté de 4 espaces pour déclarer une structure de code qui est à l'intérieur d'une instruction. 


```
Si ceci:
    alors fais cela


mais cette instruction sera toujours exécutée
```
p.s. python est très pointilleux là-dessus... un "tab" n'est pas égal à 4 espaces.



## Les conditions
En programmation, il est important de définir des conditions afin d'aguiller les controleur de flow. Les conditions génèrent une booléen (vrai ou faux).



### opérateur `=` vs `==` (vs `===`)
On a 3 opérateurs distincts


* l'opérateur `=` permet d'attribuer une valeur à une variable.  
* l'opérateur `==` permet de comparer 2 valeurs  
* l'opérateur `===` est une abomination javascript, parce que selon JS, 2 == "2"  


Ainsi, quand on fait un `if` avec 
```
if ma_variable = 4:
    fait ceci
```
on aura toujours vrai, parce que python est toujours capable d'attribuer 4 à la variable `ma_variable`.


### opérateur `!`
l'opérateur `!` permet d'inverser une conclusion logique et ainsi d'exécuter du code lorsque la condition est fausse


```
if `ma_variable != 4:
   `ma_variable` = 1
```


### opérateur logique `and` et `or`
Ces opérateur permettent de combiner deux conditions ensemble. Le `and` dit `vrai` si les deux conditions sont vraies, le `or` dit `vrai` si un ou l'autre (ou les deux) conditions sont vraies.

```
ma_variable = 2
ta_variable = 4

if ma_variable < ta_variable and ta_variable > 0:
    print("ok tu gagnes")

if ma_variable < 0 or ta_variable > 0 :
    print("soit je suis sous zéro, soit tu es plus grand que 0, ou les deux")

```

Ces opérateurs sont parfois appeller des "gates", on aussi les Xor, mais on embarquera pas la-dedans




## if / else / elif
Le `if` est sans doute le controle de flow le plus utilisé. Tout dans la vie est une if; chaque prise de toute de décision est conclue sur "oui" ou "non", "vrai" ou "faux". C'est ça aussi dans un logiciel. 


```
ma variable = 4
if `ma_variable` >= 2:
    `ma_variable` += 1


ta variable = 5
if `ma_variable` > `ta_variable`:
    print("je gagne")
elif `ma_variable` < `ta_variable`:
    print("tu gagnes")
else:
    print("c'est nul RIP")
```


## while
Le `while` est un contrôleur qui continue à exécuter une boucle de code tant et aussi longtemps, qu'à la fin de la boucle, la condition qu'il évalue soit vraie. Il s'agit d'un contrôleur potentiellement dangereux, car il est possible que la condition soit toujours vraie.


```language=python
ma_variable = 0
while `ma_variable` < 5 :
    print(`ma_variable`) # imprimera 0, 1, 2, 3, 4
    `ma_variable` += 1 # fera 5 itérations


while `ma_variable > 3: 
    print(`ma_variable`) # imprimera 5, 6, 7, ....
    `ma_variable` += 1 # et n'arrêtera jamais (car `ma_variable` sera toujours > 3)
```


## for...in
le `for...in` est associé à une variable qui contient une séquence d'éléments. On exécute un traitement pour chacun des éléments de cette séquence. Attention, on ne doit jamais toucher à l'itérable sous-jacent.


```
ma_liste = [1, 2, 3, 4]


for mon_element in ma_list:
    print(mon_element) # imprimera 1, 2, 3
    print(mon_element + 1) # imprimera 2, 3, 4
    if mon_element == 4:
        print("4 le chiffre du diable")
        break 

```


La boucle `for ... in` est aussi une boucle `while`.
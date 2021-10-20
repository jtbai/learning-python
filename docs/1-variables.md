# Variables
Les variables sont l'unité de base en programmation. Elle servent a stocker de l'information pour être traitée par la suite.
Les variables ont leur de leur création un type qu'ils conservent tout au long de leur vie. On assigne une variable à un symbole avec l'opérateur `=`

```
  symbole = 1
  autre_symbole = "bonjour"
  nimporte_quoi_finalement = 2.3563
```


## Les types de base 
Les types de base sont les items les plus utilisés. 

1. bool: Booléen (vrai ou faux) 
2. int: Entier (0,1,2,3,4)
3. float: Nombre à virgule (1.12, 3.141592654)
4. str: Chaine de caractère ("bonjour", "1234")

## Les types plus avancées
Les types plus avancées permettent de mieux gérer des ensemble de variables afin de creer des groupes logiques. 


1. list: liste de variables indexée séquentiellement. L'ordre d'insertion est conservé
  ```
    ma_list = ["a","b","c"]
    ma_list[4] = ["w"]
    ma_list[2] # retourne "c" - oui "c" et non pas "b", car python compte à partir de 0
  ```
2. dict: tableau associatifs entre une "clé" et une "valeur". L'ordre n'existe pas dans cette structure
  ```
    mon_dict = {"cle1":"valeur1", "cléx":234, "whatever":ma_list}
    mon_dict["nouvelle_clé"] = "valeur de la nouvelle clé"
    
    mon_dict["cle1"] # retourne "valeur1"
    mon_dict[cle1] # retourne une erreur parce que la variable `cle1` n'existe pas
    mon_dict[1] # Creer une erreur car la clé 1 n'Existe pas, même s'il y a plus d'une clé
    
  ```

## Les méthodes
Les méthodse sont des opérations qui s'effectuent sur la variable. 
* [`int`, `float` (Types numériques)](https://docs.python.org/3.10/library/stdtypes.html#typesnumeric)
* [`str` (chaînes de caractères)](https://docs.python.org/3.10/library/stdtypes.html#str)
* [`list` (Sequence)](https://docs.python.org/3.10/library/stdtypes.html#list)
* [`dict` (Types associatif)](https://docs.python.org/3.10/library/stdtypes.html#dict)

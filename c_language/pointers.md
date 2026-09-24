# Pointeurs in C
> Les variables déclarées sont stockées en mémoire centrale. Cette même mémoire est composée d'octets idientifiable par ce qu'on appelle une *adrese*.

* Pour retrouver une variable, il faut connaître l'adresse. 
* Le nom de variable est son idendantificateur, le compilateur fait le lien entre le nom de variable et son adresse.

```mermaid
flowchart TD
variable --> object --> i
variable --> adresse --> 4831836000
variable --> valeur --> 3

```
---
une adresse à un type LONG (64 bits)
---

* L'opératuer & permet d'accéder à l'adresse mémoire
  * son retour est une constante, elle ne peut pas être modifé par une affectation <br>`variable = expression`

* un pointeur est un objet dont la valeur est égale à l'adresse mémoire.
  * `type *foo`

```mermaid
flowchart TD

psid[4831836000]
variable --> object --> i
variable --> adresse --> 4831836000
variable --> valeur --> 3

pointeur --> object_p --> p
pointeur --> adresse_p --> 4831836004
pointeur --> valeur_p --> psid
```

Exemple type : 
```c
main()
{
    int i = 3;
    int *p;

    p = &i;
    printf("*p = %d \n, *p");
}
```

|name|type|e|
|--|--|--|
|i|int|3|
|*p|int|3 (accède à l'adresse mémoire contenu dans p)|
|p|pointer|4831836000|

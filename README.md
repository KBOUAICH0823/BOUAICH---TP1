# BOUAICH---TP
Exercice 1:
Algorithme_Pin
    VAR code saisie , erreur :entier
    CONS code pin:entier
Debut
    Pour i de 1 a 3 faire
       ecrire("saisie le code pin:")
       lire (pin_saisie)
       Si code pin=code saisie alors
          ecrire("operation fait avec succes")
         sinon
          Erreur←erreur+1
          Ecrire("erreur")
        Fin si
     Fin pour
   Si erreur=3 alors
       Ecrire ("carte SIM bloque")
    Fin si
Fin

          Exercice 2
Algorithme_l'echange
   Var a,b,c:entier
Debut
  Ecrire("donner la valeur de a et b")
   Lire (a,b)
   c←a
   a←b
    b←c
    ecrire("a=", a , "b=",b)
Fin

            Exercice 3
1} Algorithme_PGCD
    VAR a,b,reste:entier
Debut
   ecrire("donner les valeurs de a et b") O(1)
    Lire (a,b) O(1)
    Tant que b# 0 faire.  O(1)
      reste←a mod b.  O(1)
       a←b.      O(1)
       b←reste.    O(1)
    Fin tant que
     ecrire("PGCD est:",a)    O(1)
Fin
  Complexite =O(log n)

2} Algorithme PGCD
    VAR a,b,reste: entier
    Fonction PGCD (a,b:entier):entier
      Si b=0 alors.      O(1)
          Retourne a.          O(1)
           Sinon
           Retourne PGCD(b,a mod b)  O(log n)
      Fin si 
     Fin fonction
Debut
  ecrire("donner les valeurs de a et b") O(1)
   Lire (a,b)          O(1)
   ecrire(" le PGCD est:" ,a)    O(1)
Fin

Complexite = O (log n)

Les complexite sont egaux

           Exercice 5
Algorithme_deviner_un_nombre
   Var secret,x,tetative:entier
   Reponse:chaine
Debut
   Repeter
      Secret←aleaoire(1,100)
      tentative←0
      Tant que tentative<= 5 faire
        ecrire("deviner un nombre:")
         Lire x
         tentative←tentative+1
          Si x=secret alors
               ecrire("felicitation")
                retourne
                Sinon
                   Si x< secret alors
                      ecrire("trop petit")
                         Sinon
                           ecrire ("trop grand")
                    Fin si 
             Fin si
        Fin tant que
     Si x # secret alors
           Ecrire("malheureusemet,le secret est:", secret)
     Fin si
      Ecrire("voulez vous rejouer? Oui ou nom")
       Lire reponse
    jusqu'a reponse =non
Fin

            Exercice 6
Algorithme_triangle_de_floyd
    VAR a,i,b:entier
     Procedure lignes(a:entier , b:entier)
       Pour j de 1 a b faire.      O(n)
          Ecrire a.          
           a←a+1
       Fin pour 
    Fin procedure
Debut
    ecrire("donner un nombre")   O(1)
    Lire b.         O(1)
     a←1.             O(1)
     Pour i de 1 a b faire
        Procedure lignes (a,b)   O(n)
         a←a+i.          O(1)
      Fin pour
Fin

Complexite= O(n²)

            Exercice 7 
1}  Algorithme_somme_des_entiers
        Var n,s,i :entier
  Debut
    ecrire("donner un nombre")   O(1)        lire n.   O(1)
    somme ← 0.       O(1)
         Pour i de 1 a n faire.     O(n)
              s ← s+1.               O(n)
         Fin pour
           Ecrire("la somme est:"s)      O(1)
Fin

Complexite = O(n)

2} ALGORITHME somme_des_entiers
         VAR nombre,somme:ENTIER
          Fonction sommeEntier (n:ENTIER): ENTIER
            Si (n = 1 ) Alors.  O(1)
                  retourne  n.   O(1)
            Sinon
                  retourne  n + sommeEntier(n-1)       O(1)
            Fin Si
      Fin Fonction

DEBUT
      
      ecrire("Donner un nombre: ")   O(1)
      lire(nombre)     O(1)
      somme <-- sommeEntier(nombre)  O(n)
      ecrire(" La somme est: ", somme) O(1)
FIN

Complexite = O(n)

Les complexites sont egaux
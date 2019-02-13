# Description
Créé lors d'un projet de groupe de licence 3.  
L'idée de ce projet est de créer un simulateur ***ARMv5*** permettant de traduire en langage machine du code assembleur ***ARMv5***, et de l'exécuter grâce à ***gdb***.  

# Détails
Le programme prend en entrée un fichier contenant un subset du jeu d'instruction **ARMv5**, et le traduit en langage machine.  
Ce code machine est ensuite interpreté par le simulateur de ***gdb*** (gdb-arm-none-eabi).  
La traduction du code en binaire est fait grâce à la documentation **ARMv5**  
Les opérations prises en comptes sont:  
- Les opérations de ***Load-Store*** permettant de d'intéragir avec la mémoire (***str, ldr***).  
- Les opérations de branchement (***b***).
- Toutes les opérations arithmétiques et leurs déclinaisons (***add***, ***sub***).

# Utilisation 
./arm-simulator    // Pour lancer le simulateur ARM, celui çi va attendre la connexion d'un client gdb.

arm-elf-gdb        // Lancement du client gdb
file exemple.txt
target remote localhost:<port donné par le simulateur>
load
.

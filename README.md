#include <stdio.h>
#include <stdlib.h>
char *ChargerChaine(int N) {
    char *chaine = (char *)malloc(N+1* sizeof(char));
    if (chaine == NULL) {
        printf("Erreur !\n");
        exit(1); 
    }
    printf("Veuillez entrer une chaîne de caractères (max %d caractères): ", N );
    fgets(chaine, N, stdin); 
    return chaine; 
} 

// 2

#include <stdio.h>
int Longueur(char *ch) {
    int longueur = 0;
    while (*ch != '\0') {
        longueur++;
        ch++; 
    }
    return longueur;
}

//3

#include <stdio.h>
#include <stdlib.h>
void ChargerTab(char *p, char Tab[]) {
    int i = 0;
    while (p[i] != '\0') {
        Tab[i] = p[i];
        i++;
    }
    Tab[i] = '\0';
}
void ChargerTab(char *p, char Tab[]);

int main() {
    int tailleMax;
    printf("Entrez la taille maximale de la chaîne : ");
    scanf("%d", &tailleMax);
     scanf("%s",chaine); 
    char *chaine = (char *)malloc(tailleMax * sizeof(char));
    if (chaine == NULL) {
        printf("Erreur d'allocation de mémoire\n");
        exit(1);
    }
    printf("Entrez une chaîne : ");
    fgets(chaine, tailleMax, stdin);
    char Tab[tailleMax];
    ChargerTab(chaine, Tab);
    printf("Le tableau des caractères est : %s\n", Tab);
    free(chaine);
    return 0;
}

\\4

#include <stdio.h>
#include <stdlib.h>
void InverserTab(char Tab[], char T[], int m) {
    int i, j;
    for (i = 0, j = m - 1; j >= 0; i++, j--) {
        T[i] = Tab[j];
    }
    T[m] = '\0'; 
}
void InverserTab(char Tab[], char T[], int m);

int main() {
    int tailleMax;
    printf("Entrez la taille maximale de la chaîne : ");
    scanf("%d", &tailleMax);
    scanf("%s",chaine); 
    char *chaine = (char *)malloc(tailleMax * sizeof(char));
    if (chaine == NULL) {
        printf("Erreur d'allocation de mémoire\n");
        exit(1);
    }
    printf("Entrez une chaîne : ");
    fgets(chaine, tailleMax, stdin); 
    int longueur = 0;
    while (chaine[longueur] != '\0' && chaine[longueur] != '\n') {
        longueur++;
    }
    chaine[longueur] = '\0';
    char TabInverse[tailleMax];
    InverserTab(chaine, TabInverse, longueur);
    printf("La chaîne inversée est : %s\n", TabInverse);
    free(chaine); 
    return 0;
}






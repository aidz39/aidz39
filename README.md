Voici comment vous pouvez écrire cet algorithme en langage C pour échanger le triangle inférieur avec 

#include <stdio.h>

void echangerTriangles(int n, int matrice[n][n]) {
    for (int i = 0; i < n; i++) {
        for (int j = i + 1; j < n; j++) {
            // Échange des éléments au-dessus et en dessous de la diagonale principale
            int temp = matrice[i][j];
            matrice[i][j] = matrice[j][i];
            matrice[j][i] = temp;
        }
    }
}

void afficherMatrice(int n, int matrice[n][n]) {
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n; j++) {
            printf("%d ", matrice[i][j]);
        }
        printf("\n");
    }
}

int main() {
    int matrice[4][4] = {
        {1, 2, 3, 4},
        {5, 6, 7, 8},
        {9, 10, 11, 12},
        {13, 14, 15, 16}
    };

    printf("Matrice avant symétrie :\n");
    afficherMatrice(4, matrice);

    echangerTriangles(4, matrice);

    printf("\nMatrice après symétrie :\n");
    afficherMatrice(4, matrice);

    return 0;
}
<!---
aidz39/aidz39 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

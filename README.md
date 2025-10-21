#include <stdio.h>
#include <string.h>
#define TOTAL_TERRITORIOS 5
typedef struct {
    char nome[50];
    char corExercito[30];
    int tropas;
} Territorio;
int main() {
    Territorio territorios[TOTAL_TERRITORIOS];

  for (int i = 0; i < TOTAL_TERRITORIOS; i++) {
        printf("\n=== Cadastro do Território %d ===\n", i + 1);
 printf("Nome do território: ");
        fgets(territorios[i].nome, sizeof(territorios[i].nome), stdin);
        territorios[i].nome[strcspn(territorios[i].nome, "\n")] = '\0';
  printf("Cor do exército: ");
        fgets(territorios[i].corExercito, sizeof(territorios[i].corExercito), stdin);
        territorios[i].corExercito[strcspn(territorios[i].corExercito, "\n")] = '\0';
 printf("Número de tropas: ");
        scanf("%d", &territorios[i].tropas);
        getchar();
    }
 printf("\n=== Estado Atual do Mapa ===\n");
    for (int i = 0; i < TOTAL_TERRITORIOS; i++) {
        printf("\nTerritório %d:\n", i + 1);
        printf("Nome: %s\n", territorios[i].nome);
        printf("Cor do Exército: %s\n", territorios[i].corExercito);
        printf("Tropas: %d\n", territorios[i].tropas);
    }
return 0;
}

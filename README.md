#include <stdio.h>

void peca_vertical(int n)
{
    if (n >= 1)
    {
        printf("Percorrendo Verticalmente\n");

        peca_vertical(n - 1);
    }
        
}

void peca_horizontal(int n)
{
    if (n >= 1)
    {
        printf("Percorrendo Horizontalmente\n");

        peca_horizontal(n - 1);
    }
}

void peca_verticalmente_esquerda(int n)
{
    if (n >= 1)
    {
        printf("Percorrendo verticalmente para esquerda\n");

        peca_verticalmente_esquerda(n - 1);
    }
}

void peca_verticalmente_direita (int n)
{
    if (n >= 1)
    {
        printf("Percorrendo verticalmente para direita\n");
        
        peca_verticalmente_direita(n - 1);
    }
}

void peca_movimento_cavalo(int movimento)
{
   for (int m = 0; m < movimento; m++)
   {

    for (int cima = 0; cima < 2; cima++)
    {
        printf("Cima\n");
    }
    
    for (int direita = 0; direita < 1; direita++)
    {
        printf("Direita\n");
    }
   }
}



int main (){
    //variaves
    int opcao;

    //Variaveis Cavalo
    int movimento_cavalo;

    //Variaveis Torre
    int movimento_torre;
    
    //Variaveis Bispo
    int movimento_bispo;

    //Variaveis Rainha
    int movimento_rainha;
    
    //Menu
    printf("===ESCOLHA UMA PECA===\n");
    printf("Torre[1]\nBispo[2]\nRainha[3]\nCavalo[4]\n");
    printf(">");
    scanf("%d", &opcao);

    //Opcao Torre
    if (opcao == 1)
    {
        printf("Mover a torre Verticalmente(1) ou mover Horizontalmente(2)\n");
        printf(">");
        scanf("%d", &movimento_torre);

        //Movimento da peça torre verticalmente
        if (movimento_torre == 1){
            
            int quantidade = 7;
            peca_vertical(quantidade);

        //Movimento da peça torre horizontalmente 
        }else if (movimento_torre == 2){

            int quantidade = 7;
            peca_horizontal(quantidade);

        } else {
            printf("opcao Invalida");
        }

    //Opcao Bispo
    } else if (opcao == 2)
    {
        printf("Mover verticalmente para Esquerda(1) ou Direita(2)\n");
        printf(">");
        scanf("%d", &movimento_bispo);

        //Movimento da peçaa bispo para esquerda
        if (movimento_bispo == 1)
        {
            int quantidade = 2;
            peca_verticalmente_esquerda(quantidade);

        //Movimento da peça bispo para direita
        } else if (movimento_bispo == 2){

            int quantidade = 5;
            peca_verticalmente_direita(quantidade);

        } else {
            printf("Opcao invalida");
        }

    //Opcao Rainha
    } else if (opcao == 3)
    {
        printf("Mover para Frente(1), Verticalmente para Esquerda(2) ou Direita(3)\n");
        printf(">");
        scanf("%d", &movimento_rainha);


        //Movimento rainha para frente
        if (movimento_rainha == 1)
        {
            int quantidade = 7;
            peca_vertical(quantidade);

        //Movimento rainha verticalmente para esquerda
        } else if (movimento_rainha == 2)
        {
            int quantidade = 3;
            peca_verticalmente_esquerda(quantidade);
        
        
        //Movimento rainha verticalmente para direita
        } else if(movimento_rainha == 3) {
            int quantidade = 4;
            peca_verticalmente_direita(quantidade);

        } else {
            printf("Opcao invalida");
        }
        
    //opcao Cavalo
    } else if (opcao == 4)
    {
        printf("Mover para direita(1) ou esquerda(2)\n");
        printf(">");
        scanf("%d", &movimento_cavalo);

        //Movimento Cavalo Cima direita
        if (movimento_cavalo == 1)
        {
            int quantidade = 3;
            peca_movimento_cavalo(quantidade);
        
        //Movimento Cavalo Cima esquerda
        } else if (movimento_cavalo == 2)
        {
            peca_movimento_cavalo(3);

        } else {
            printf("Opcao Invalida");
        }

    //Opção inválida
    } else {
        printf("opcao Invalida\n");
    }
    
    
    return 0;
}

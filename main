import java.util.Scanner;

public class Main {
    static void Inicial() {
        // Tela Inicial
        
        System.out.println("========== CONTROLE DE ESTOQUE ® ==========");
        System.out.println("Aplicação por Jefferson Sant'ana e Helana Sousa");
        System.out.println("Direitos de cópia reservado\n");
        
    }
        
    static void Menu() {
        System.out.println("\n--- MENU ---");
        System.out.println("Selecione: \n[1] - CONSULTA DE ESTOQUE\n[2] - ENCERRAR APLICATIVO");
    }
    

    public static void main(String[] args) {
        // LOADING DE SCANNER E TELA INICIAL
        int menu = 0; 
        Scanner teclado = new Scanner(System.in);
        Inicial();

                // CADASTRO DE NOVOS PRODUTOS
        System.out.println("=== CADASTRO DE PRODUTOS ===");
        System.out.println("Insira a quantidade de produtos a serem cadastrados: ");
        int col = teclado.nextInt();          
         
        int[] codBarras = new int[col];
        float[] preco = new float[col]; 
        int i;
        
        cadastro:
        for (i = 0;i<col;i++){
            System.out.println("Produto " + (i + 1) + "- Digite código de barras ou 0 para encerrar: ");
            codBarras[i] = teclado.nextInt();
            if (codBarras[i] != 0 ){
                System.out.println("Insira o preço do produto " + codBarras[i] + ": (ex: 10.99) ");
                preco[i] = teclado.nextFloat();}
                if(codBarras[i] == 0){
                    System.out.println("Fim do cadastro");
                    break cadastro;
                    }
                    }
                  
            do{
            Menu();
            menu = teclado.nextInt();
            if (menu == 1){

                System.out.println("=== CONSULTA DE ESTOQUE ===");
                System.out.println("Insira o índice do produto a ser consultado (iniciando em 1)\nou digite [0] para mostrar todo o estoque: ");
                int z = 0;
                z = teclado.nextInt();
                z --;
                all:
                if (z == -1){
                    for (i = 0; i<codBarras.length;i++){
                        if (codBarras[i] == 0){
                            break all;
                        }   
                        else{
                            System.out.println(codBarras[i] + ": R$" + preco[i]);
                        }
                    }
                }
           
                else {
                    System.out.println(codBarras[z] + ": R$" + preco[z]);
                                    }
            }
                
            else {
                System.out.println("TODOS OS DADOS SERÃO PERDIDOS, DESEJA CONTINUAR? \n[0] - NÃO\n[1] - SIM");
                int desligar = teclado.nextInt();
                if (desligar == 1){
                    System.exit(0);
                                    }
                }

        }
        while (menu != 1 || menu != 2);{
            System.out.println("Opção Inválida. Tente novamente");
        }
   }
}



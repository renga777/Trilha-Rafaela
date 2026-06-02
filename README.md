# Trilha-Rafaela
Codigo da trilha da Rafela : 

Segue abaixo o codigo : 

# Sistema de Folha de Pagamento em Java

```java
import java.util.ArrayList;
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        final double SALARIO_BASE = 2000;

        ArrayList<String> nomes = new ArrayList<>();
        ArrayList<Integer> matriculas = new ArrayList<>();
        ArrayList<Double> salarios = new ArrayList<>();

        int opcao;

        do {

            System.out.println("\n===== MENU =====");
            System.out.println("1 - Funcionário Padrão");
            System.out.println("2 - Funcionário Comissionado");
            System.out.println("3 - Funcionário Produção");
            System.out.println("4 - Mostrar Folha");
            System.out.println("0 - Sair");

            System.out.print("Escolha: ");
            opcao = sc.nextInt();
            sc.nextLine();

            switch(opcao) {

                case 1:

                    System.out.print("Nome: ");
                    String nome = sc.nextLine();

                    System.out.print("Matrícula: ");
                    int matricula = sc.nextInt();

                    nomes.add(nome);
                    matriculas.add(matricula);
                    salarios.add(SALARIO_BASE);

                    System.out.println("Funcionário cadastrado!");
                    break;

                case 2:

                    System.out.print("Nome: ");
                    String nome2 = sc.nextLine();

                    System.out.print("Matrícula: ");
                    int matricula2 = sc.nextInt();

                    System.out.print("Valor das vendas: ");
                    double vendas = sc.nextDouble();

                    System.out.print("Percentual da comissão: ");
                    double percentual = sc.nextDouble();

                    double comissao = vendas * percentual / 100;

                    double salarioFinal = SALARIO_BASE + comissao;

                    nomes.add(nome2);
                    matriculas.add(matricula2);
                    salarios.add(salarioFinal);

                    System.out.println("Funcionário cadastrado!");
                    break;

                case 3:

                    System.out.print("Nome: ");
                    String nome3 = sc.nextLine();

                    System.out.print("Matrícula: ");
                    int matricula3 = sc.nextInt();

                    System.out.print("Quantidade de peças: ");
                    int quantidade = sc.nextInt();

                    System.out.print("Valor por peça: ");
                    double valorPeca = sc.nextDouble();

                    double bonus = quantidade * valorPeca;

                    double salarioProducao = SALARIO_BASE + bonus;

                    nomes.add(nome3);
                    matriculas.add(matricula3);
                    salarios.add(salarioProducao);

                    System.out.println("Funcionário cadastrado!");
                    break;

                case 4:

                    System.out.println("\n===== FOLHA DE PAGAMENTO =====");

                    System.out.println("Total de funcionários: " + nomes.size());

                    for(int i = 0; i < nomes.size(); i++) {

                        System.out.println("\nNome: " + nomes.get(i));
                        System.out.println("Matrícula: " + matriculas.get(i));
                        System.out.println("Salário Final: " + salarios.get(i));
                    }

                    break;

                case 0:

                    System.out.println("Programa encerrado!");
                    break;

                default:

                    System.out.println("Opção inválida!");

            }

        } while(opcao != 0);

        sc.close();
    }
}
```


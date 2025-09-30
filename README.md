import java.util.Scanner;

public class CalculoDeMedias {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        System.out.println("=== SISTEMA ESCOLAR - CÁLCULO DE MÉDIAS ===\n");

        double[] notas = new double[8];
        for (int i = 0; i < 8; i++) {
            System.out.print("Digite a nota " + (i + 1) + ": ");
            notas[i] = scanner.nextDouble();
        }

        double[] mediasBimestrais = new double[4];
        for (int i = 0; i < 4; i++) {
            mediasBimestrais[i] = (notas[i * 2] + notas[i * 2 + 1]) / 2.0;
        }

        double media1Semestre = (mediasBimestrais[0] + mediasBimestrais[1]) / 2.0;
        double media2Semestre = (mediasBimestrais[2] + mediasBimestrais[3]) / 2.0;

        double mediaFinal = (media1Semestre + media2Semestre) / 2.0;

        System.out.println("\nPráticas\n");

        System.out.printf("1o Bimestre: %.1f%n", mediasBimestrais[0]);
        System.out.printf("2o Bimestre: %.1f%n", mediasBimestrais[1]);
        System.out.printf("1o Semestre: %.1f%n", media1Semestre);
        System.out.println("----------------------");

        System.out.printf("3o Bimestre: %.1f%n", mediasBimestrais[2]);
        System.out.printf("4o Bimestre: %.1f%n", mediasBimestrais[3]);
        System.out.printf("2o Semestre: %.1f%n", media2Semestre);
        System.out.println("-----------------------");

        System.out.printf("Média Final: %.1f%n", mediaFinal);

        scanner.close();
    }
}





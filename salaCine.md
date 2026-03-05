import java.util.Scanner;

public class SalaCine {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);
  
        int[][] asientos = new int[3][4];

        System.out.print("Ingrese fila (0 a 2): ");
        int f = sc.nextInt();

        System.out.print("Ingrese columna (0 a 3): ");
        int c = sc.nextInt();


        if (f >= 0 && f < 3 && c >= 0 && c < 4) {

            if (asientos[f][c] == 0) {
                asientos[f][c] = 1;
                System.out.println("Asiento reservado correctamente.");
            } else {
                System.out.println("Ese asiento ya está reservado.");
            }

        } else {
            System.out.println("Posición inválida.");
        }

        System.out.println("\nEstado de la sala:");

        for (int i = 0; i < 3; i++) {
            for (int j = 0; j < 4; j++) {
                System.out.print(asientos[i][j] + " ");
            }
            System.out.println();
        }

        sc.close();
    }
}

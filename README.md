# Laboratorio-1-BM01
Implementar un programa que resuelve una sucesión numérica.
import java.util.Scanner;

public class SumatoriaSerieS {

    public static void main(String[] args) {
        // Declaramos las variables
        int n;
        int i;
        int sumatoria;

        // Obtenemos el valor de n del usuario
        Scanner sc = new Scanner(System.in);
        System.out.print("Ingrese el valor de n: ");
        n = sc.nextInt();

        // Inicializamos la sumatoria en 0
        sumatoria = 0;

        // Iteramos desde 1 hasta n
        for (i = 1; i <= n; i++) {
            // Calculamos el término actual
            int termino = calculaTermino(i);

            // Sumamos el término actual a la sumatoria
            sumatoria += termino;

            // Imprimimos el término actual
            System.out.print(termino + " ");
        }

        // Imprimimos la sumatoria
        System.out.println();
        System.out.println("La sumatoria es: " + sumatoria);
    }

    // Calcula el término i de la sucesión S
    private static int calculaTermino(int i) {
        // Si i es par
        if (i % 2 == 0) {
            // El término es 2/i
            return 2 / i;
        } else {
            // El término es
            // -(5/(i * (i + 1)))
            return -(5 / (i * (i + 1)));
        }
    }
}

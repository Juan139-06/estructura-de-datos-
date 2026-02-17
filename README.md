public class Fibonacci {

    // Método que devuelve el n-ésimo número de Fibonacci
    public static long fibonacci(int n) {
        if (n <= 0) {
            throw new IllegalArgumentException("El número debe ser mayor que 0");
        }
        if (n == 1 || n == 2) {
            return 1;
        }

        long anterior = 1;
        long actual = 1;
        long siguiente = 0;

        for (int i = 3; i <= n; i++) {
            siguiente = anterior + actual;
            anterior = actual;
            actual = siguiente;
        }

        return actual;
    }

    public static void main(String[] args) {
        int numero = 10;
        System.out.println("El número Fibonacci en la posición " + numero + " es: " + fibonacci(numero));
    }
}

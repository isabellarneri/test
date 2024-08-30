# test
int main() {
    int num, a = 0, b = 1, fib = 0;

    // Solicita ao usuário um número
    printf("Informe um número: ");
    scanf("%d", &num);

    if (num == 0) {
        printf("O número %d pertence à sequência de Fibonacci.\n", num);
        return 0;
    }

    while (fib < num) {
        fib = a + b; // Calcula o próximo número da sequência
        a = b;       // Atualiza o valor de 'a' para o próximo cálculo
        b = fib;     // Atualiza o valor de 'b' para o próximo cálculo
    }

    // Verifica se o número informado é igual ao último número da sequência calculada
    if (fib == num) {
        printf("O número %d pertence à sequência de Fibonacci.\n", num);
    } else {
        printf("O número %d não pertence à sequência de Fibonacci.\n", num);
    }

    return 0;
}

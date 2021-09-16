* **Desafio:** Nesse desafio você terá que desenvolver um programa que leia um valor e apresente o número de Fibonacci correspondente a este valor lido. Lembre que os 2 primeiros elementos da série de Fibonacci são 0 e 1 e cada próximo termo é a soma dos 2 anteriores a ele. Todos os valores de Fibonacci calculados neste problema devem caber em um inteiro de 64 bits sem sinal.  

* **Entrada:** A primeira linha da entrada contém um inteiro T, indicando o número de casos de teste. Cada caso de teste contém um único inteiro N (0 ≤ N ≤ 60), correspondente ao enésimo termo da série de Fibonacci.

* **Saída:** Para cada caso de teste da entrada, imprima a mensagem "Fib(N) = X", onde X é o N-ésimo termo da série de Fibonacci.

* **Resolução:**
```
import java.io.IOException;
import java.util.Scanner;

public class FibonacciEmVetor{
    
    public static void main(String[] args) throws IOException {
        Scanner leitor = new Scanner(System.in);
        int T = leitor.nextInt();
        
        //Verifica o número de casos de testes até chegar no T informado
        for (int casos = 0; casos < T; casos++) {
            int N = leitor.nextInt(); 
            long anterior = 0, atual = 1, proximo;
            
            //Até atingir o N
            for (int valor = 0; valor < N; valor++ ) {
                proximo = atual; //não tenho valor de próximo, se torna atual
                atual = atual + anterior; //soma do próximo
                anterior = proximo; //anterior do próximo
            }
            System.out.println("Fib("+ N +") = " + anterior);
        }
    }
    
}
```
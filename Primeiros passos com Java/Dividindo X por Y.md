* **Desafio:** Você terá o desafio de escrever um algoritmo que leia 2 números e imprima o resultado da divisão do primeiro pelo segundo. Caso não for possível, mostre a mensagem “divisao impossivel” para os valores em questão.  

* **Entrada:** A entrada contém um número inteiro N. Este N será a quantidade de pares de valores inteiros (X e Y) que serão lidos em seguida.

* **Saída:** Para cada caso mostre o resultado da divisão com um dígito após o ponto decimal, ou “divisao impossivel” caso não seja possível efetuar o cálculo.

* **Resolução:**
```
import java.io.IOException;
import java.util.Scanner;

public class Problem {
	
    public static void main(String[] args) throws IOException {
		//complete os espaços com sua solução
                Scanner leitor = new Scanner(System.in);
		int N = leitor.nextInt();
		int X, Y;
		for (int i = 0; i < N; i++) {
			X = leitor.nextInt();
			Y = leitor.nextInt();
			if (Y == 0) {
			  System.out.println("divisao impossivel"); //Divisor 0 = divisão indefinida
			} else { 
			  double divisao = (double) X / Y; //Pode dar valor com vírgula
			  System.out.printf("%.1f\n", divisao); // 1 casa 
			}
		}
		
		leitor.close();
		
    }
	
}
```
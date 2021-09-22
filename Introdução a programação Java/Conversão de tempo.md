* **Desafio:** Você terá o desafio de ler um valor inteiro, que é o tempo de duração em segundos de um determinado evento em uma loja, e informe-o expresso no formato horas:minutos:segundos.

* **Entrada:** O arquivo de entrada contém um valor inteiro N.

* **Saída:** Imprima o tempo lido no arquivo de entrada (segundos), convertido para horas:minutos:segundos, conforme exemplo fornecido.

* **Resolução:**
```
import java.util.Scanner;

public class ConversaoTempo {

     public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        int sec;
        sec = input.nextInt();
        int hour = sec / 3600;
        sec %= 3600; //resto da divisão 

        int min = sec / 60;
        sec %= 60; //resto da divisão

        System.out.println(hour + ":" + min + ":" + sec);
    }
}
```
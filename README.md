# Aprendizados_Java
package Fundamentos;
import java.util.Date;
public class TesteFund {
    public static void main(String[] args){
        var F=86; //variavel

        final var x = 32; //constante
        final var y= 5/9.0;
//(F-32)* 5/9 = C
        var C = (F-x)*y; //variavel

        System.out.println("a conversao de fa para celcius = " + C);

        boolean SalarioCaiu = false;//true or false
        char status= 'Q'; // so pode botar uma letra
        String BD = "Bom dia X";

        BD=BD.toUpperCase();
        System.out.println(BD);

       BD=BD.replace("X", "Senhora");
        System.out.println("Hello Wolrd".concat(" !!!"));

        String BT= "Boa tarde" .replace("tarde","Noite");
        System.out.println(BT);
        String Contact = "Bom".concat(" Diaaa").toLowerCase();
        System.out.println(Contact);

        Date d = new Date();
        System.out.println(d);

        Scanner teclado = new Scanner(System.in);
 
    System.out.println("Qual a sua idade?");
    int idade = teclado.nextInt();
    System.out.println("Qual o seu nome?");
    String nome = teclado.nextLine();
    System.out.println("Qual o seu sobrenome?");
    String sobrenome = teclado.nextLine();
 
    teclado.close();
    }

}
exercicios sexta 

package Fundamentos;

import java.util.Scanner;

public class Shopping {
    public static void main (String [] args){
        Scanner entrada = new Scanner(System.in);

        System.out.println("Está Sol neste momento ?");
        String sol = entrada.next();

        System.out.println("Es?");

        entrada.close();
        System.out.println(sol);

    }
}
 exercicios sexta 
 package Fundamentos;
import java.util.Locale;
import java.util.Scanner;
public class scan {

        public static void main(String[] args) {

            Scanner scanner = new Scanner(System.in);

            System.out.println("Digite o valor do seu salario desse mes  : ");
            String salario1 = scanner.next().replace(",",".");

            System.out.print("Digite o valor do seu salario no ultimo mes : ");
            String salario2 = scanner.next().replace(",",".");

            System.out.print("Digite o valor do seu salario de dois meses atras : ");
            String salario3 = scanner.next().replace(",",".");


            double valor1 = Double.parseDouble(salario1);
            double valor2 = Double.parseDouble(salario2);
            double valor3 = Double.parseDouble(salario3);


            double media = (valor1+valor2+valor3) / 3;

            System.out.println("Media salarial :"+media);


            scanner.close();
            System.out.println(Locale.getDefault());


        }

}
exercicios sexta 
package Fundamentos;

import java.util.Scanner;

public class wrapper {
    public static void main( String [] args){
        Byte b = 100;
        Long l = 100000L;
        Short s = 1000;

        Scanner entrada = new Scanner(System.in);

        System.out.println("Digite o numero do departamento do BRB : ");
        int departamento = entrada.nextInt();


        System.out.println(b.byteValue());
        System.out.println(l.longValue());
        System.out.println(s.toString());


        System.out.println("Departamendo Digitado : "+departamento);

        entrada.close();
        Boolean bo = Boolean.parseBoolean("false");
        System.out.println(bo);
        if (bo==true){
            System.out.println("O boolean esta correto!");
        }else {
            System.out.println("o boolean esta errado");
        }

    }
}

exercicios sexta 



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


Desafio Modulo : 
data.java: 
package ClasseMetodos;

public class Data {
    int dia;
    String mes;
    int ano;

     Data (){
        //dia = 1;
       // mes = "Janeiro";
        //ano = 1970;
         this(1,"janeiro",1970);
    }

    Data (Integer dia, String mes, Integer anoInicial){
        this.dia = dia;
        this.mes = mes;
        ano = anoInicial;
    }
     final String formatoData = "Hoje é %d de %s de %d ";

       String obterDataformata (){
         return String.format(formatoData,dia,mes,ano);
    }
    void imprimirData(){
        System.out.println(obterDataformata());
    }
}
dataTeste.java :
package ClasseMetodos;

import java.util.Scanner;

public class DataTeste {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        System.out.printf("Digite um mes:");
        String mes = entrada.nextLine();
        System.out.printf("Digite um ano:");
        int ano = Integer.parseInt(entrada.nextLine());
        System.out.printf("Digite um dia:");
        int dia = Integer.parseInt(entrada.nextLine());

        Data d1 = new Data(dia,mes,ano);

        var d2 = new Data();


        System.out.println(d1.obterDataformata());
        System.out.println(d2.obterDataformata());
    }
}


produto.java:
package ClasseMetodos;

public class Produto  {
    String nome;
    double valor;
    static double desconto = 0.30;

    Produto(){
    }
    Produto(String nomeInicial, Double precoInicial){
        nome = nomeInicial;
        valor = precoInicial;
       // desconto = descontoInicial;
    }
    double precoComdesconto (){
        return valor * (1-desconto);
    }
    double precoComdesconto (double descontoDogerente){
        return valor * (1-desconto+descontoDogerente);
    }
}

produtoTeste.java:
package ClasseMetodos;

import java.util.Scanner;

public class ProdutoTeste {
    public static void main(String[] args) {

        Produto p1 = new Produto("Mesa",300.99);

        var p2 = new Produto();
        p2.nome = "cadeira";
        p2.valor = 250.99;
        //p2.desconto = 0.50;



        System.out.printf("Os produtos comprados foram %s e %s.\n",p1.nome,p2.nome);


        double ProdutoFinal1 = p1.precoComdesconto();
        double ProdutoFinal2 = p2.precoComdesconto();
        double MediaCarinho = (ProdutoFinal1+ProdutoFinal2)/2;
        double SomaProdutos = ProdutoFinal1+ProdutoFinal2;


        System.out.println(ProdutoFinal2);

        System.out.printf("Media do seu carrinho é R$:%.2f\n",MediaCarinho);
        System.out.printf("O valor total do seu carrinho (Com descontos aplicados) :%.2f\n",SomaProdutos);
        System.out.printf("O valor do Produto 1 é : %.2f ",ProdutoFinal1);


    }
}

ValorXReferencia.java:
package ClasseMetodos;

public class ValorXReferencia {
    public static void main(String[] args) {
        double a = 2;
        double b = a; // Atribuição por valor
        a++;
        b--;

        System.out.println(a + "  " + b);

        Data d1 = new Data(26,"janeiro",2006);//Atribuição por referencia ( objeto )
        Data d2 = d1;

        System.out.println(d2.obterDataformata());

        VoltarValorPadraoData(d1);

        System.out.println(d1.obterDataformata());
        System.out.println(d2.obterDataformata());
    }
    static void VoltarValorPadraoData(Data d){
        d.mes = "agosto";
        d.dia = 1;
        d.ano = 2025;
    }
}





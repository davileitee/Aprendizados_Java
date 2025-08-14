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
    }

}

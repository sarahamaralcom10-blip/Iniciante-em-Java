import java.util.Scanner;

public class IfElse {
    public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);


        String observacao = " ";


        System.out.print(" Hora inicial da partida de futebool:");
        int Inicio = scanner.nextInt();

        System.out.print("Hora final da partida de Futebool:");
        int Final = scanner.nextInt();

        int duracao;

        if (Final > Inicio) {
            duracao = Final - Inicio;
            observacao = "O jogo começou e terminou no mesmo dia.";
          } else {
            duracao = (24 - Inicio) + Final;
             observacao = "O jogo terminou no dia seguinte.";

        }

        String Periodo = " ";
        if (Inicio >= 5 && Inicio < 12) {
           Periodo = "Manhã";

         }else if (Inicio >= 12 && Inicio < 18){
            Periodo = "Tarde";

          } else if (Inicio >= 18 && Inicio < 24 ){
             Periodo = "Noite";

            }else {
                Periodo = "Madrugada";
        }

        String Perido2 = " ";
        if (Final >= 5 && Final < 12){
            Perido2 = "Manhã";

        }else if( Final >= 12 && Final < 18){
            Perido2 = "Tarde";

        }else if (Final >= 18 && Final < 24 ){
            Perido2 = "Noite";

        }else {
            Perido2 = "Madrugada";
        }

        System.out.println(" O  jogo durou "+ duracao + " horas");
        System.out.println("Horario de inicio  " + Inicio + " da " + Periodo );
        System.out.println("Hora do termino " + Final + " da " + Perido2);
        System.out.println(" Status: " + observacao);
    }
    }

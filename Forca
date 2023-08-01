import java.io.IOException;
import java.util.Arrays;
import java.util.HashMap;
import java.util.Map;
import java.util.Scanner;

public class Main
{

    public static void main(String[] args) throws IOException
    {
        Map<Integer, String> desenhoForca = new HashMap<Integer, String>();
        desenhoForca.put(0,"+---+\n" +
                "|   |\n" +
                "    |\n" +
                "    |\n" +
                "    |\n" +
                "    |\n" +
                "=========");
        desenhoForca.put(1,"+---+\n" +
                "|   |\n" +
                "O   |\n" +
                "    |\n" +
                "    |\n" +
                "    |\n" +
                "=========");
        desenhoForca.put(2,"+---+\n" +
                "|   |\n" +
                "O   |\n" +
                "|   |\n" +
                "    |\n" +
                "    |\n" +
                "=========");
        desenhoForca.put(3,"+---+\n" +
                "|    |\n" +
                "O    |\n" +
                "/|   |\n" +
                "     |\n" +
                "     |\n" +
                "=========");
        desenhoForca.put(4,"+---+\n" +
                "|     |\n" +
                "O     |\n" +
                "/|\\   |\n" +
                "      |\n" +
                "      |\n" +
                "=========");

        desenhoForca.put(5,"+---+\n" +
                "|     |\n" +
                "O     |\n" +
                "/|\\   |\n" +
                "/     |\n" +
                "      |\n" +
                "=========");

        desenhoForca.put(6,"+---+\n" +
                "|     |\n" +
                "O     |\n" +
                "/|\\   |\n" +
                "/ \\   |\n" +
                "      |\n" +
                "=========");

        Scanner input = new Scanner(System.in);
        System.out.print("Digite a palavra da forca: ");
        String palavra = input.nextLine();

        for (int i = 0; i < 50; ++i) System.out.println();

        String vetorPalavra[] = new String[palavra.length()];
        int x =0;
        for ( String ignored : vetorPalavra) {
            vetorPalavra[x]="_";
            System.out.print(vetorPalavra[x]);
            x++;
        }

        Boolean ganhou =false;

        int contador=0;
        while (contador<7)
        {
            Boolean acertou=false;
            System.out.print("\n Digite uma letra: ");
            String letra = input.next();

            char[] chars = palavra.toCharArray();
            int y =0;
            for ( char l : chars)
            {
                if (letra.charAt(0)==chars[y])
                {
                    vetorPalavra[y]= String.valueOf(letra.charAt(0));
                    acertou=true;
                }
                y++;
            }

            if (acertou==false)
            {
                contador++;
            }

            System.out.println("\n"+desenhoForca.get(contador));
            int a =0;
            for ( char l : chars)
            {
                 System.out.print(vetorPalavra[a]);
                 a++;
            }

            if (Arrays.stream(vetorPalavra).toList().indexOf("_")==-1)
            {
                System.out.println("\n Você ganhou ! :) ");
                ganhou=true;
                break;
            }
        }
        if (ganhou==false)
        {
            System.out.println( " \n Deu forca, Voce perdeu! :(");
        }
    }
}




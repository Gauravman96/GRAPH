import java.util.Scanner;

public class adjacnecy_matrix {
    public adjacnecy_matrix() {
    }

    public static void main(String[] var0) {
        Scanner var1 = new Scanner(System.in);
        System.out.println("Enter the number of Verteces:");

        int var2;
        for(var2 = var1.nextInt(); var2 < 0; var2 = var1.nextInt()) {
            System.out.println("Enter the valid Vertices : ");
        }

        int[][] var3 = new int[var2][var2];

        int var4;
        int var5;
        for(var4 = 0; var4 < var2; ++var4) {
            for(var5 = 0; var5 < var2; ++var5) {
                System.out.println("Enter 1 if there is an edge between " + var4 + " and " + var5 + "else, enter 0");
                int var6 = var1.nextInt();
                if (var6 != 0 && var6 != 1) {
                    System.out.println("Enter the valid Edge : ");
                    var6 = var1.nextInt();
                }

                var3[var4][var5] = var6;
                var3[var5][var4] = var6;
            }
        }

        System.out.println("Printing the 2d Matrix: ");

        for(var4 = 0; var4 < var2; ++var4) {
            for(var5 = 0; var5 < var2; ++var5) {
                System.out.print(var3[var4][var5] + " ");
            }

            System.out.println();
        }

    }
}

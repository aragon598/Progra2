# Progra2
-------
import java.util.Scanner;
    
   public class SumaRecursividad{
   
    static Scanner entrada = new Scanner(System.in);
    
    static int SumaRecursivaVector(int [] vector1, int [] vector2, int n){
        if (n == 0)
            return vector1[n] + vector2[n];
        else
            return vector1[n] + vector2[n] + SumaRecursivaVector(vector1, vector2, n-1);
    }
   
    public static void main(String[] args) {
      
        int n;
        
        System.out.print("Favor ingrese el valor de N: ");
        n = entrada.nextInt();
        
        int[] vector1 = new int[n];
        int[] vector2 = new int[n];
        
        
        for(int i = 0; i < n; i++){
           vector1[i] = (int)(Math.random() * 1001);
           vector2[i] = (int)(Math.random() * 1001);
        }
        
        for(int i = 0; i < n; i++)
            System.out.print(vector1[i] + "\t");
        System.out.print("");
        for(int i = 0; i < n; i++)
            System.out.print(vector2[i] + "\t");
        
        System.out.print(" La suma de los datos de los vectores es: " + SumaRecursivaVector(vector1, vector2, n-1));
    }
    

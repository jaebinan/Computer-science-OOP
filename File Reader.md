Computer-science-OOP
====================

import java.io.BufferedReader;
import java.util.Scanner;
import java.io.*;

public class MainOOP{
  public static void main(String args[]) throws Exception{
    
    try{
      Scanner in = new Scanner(new FileReader("DRUGZZ.txt"));
      String x;
      String[] u;
      int lineCounter = 0;
      while((x=in.nextLine()) != null){
        u = x.split(" ");
        for(int i =0; i<20;i++){
          u[i] = in.nextLine();
          System.out.println(u[i]);
          
        }
        lineCounter++;
}
    System.out.println(lineCounter); 
    }catch (Exception e){
      if(e.getMessage().equals("No line found")){
        System.out.print("");
     }else{
      System.out.println("There is an error: " + e.getMessage());
     
}
}
}
}






                  
          
 

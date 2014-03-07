Computer-science-OOP
====================

import java.util.Scanner;
import java.io.*;

public class MainOOP{
  public static void main(String args[]) throws Exception{
    int lineCounter = 0;
    try{
      Scanner in = new Scanner(new FileReader("DRUGZZ.txt"));
      String x;
      String u[];
      int i = 0;
      while((x = in.nextLine()) != null){
          u = x.split(" ");
          u[i] = x;
          System.out.println(u[i]);
          lineCounter++;
          i++;
}
    }catch (Exception e){
      if(e.getMessage().equals("No line found")){
        System.out.print("");
     }else{
      System.out.println("There is an error: " + e.getMessage());
     
}
}
    //System.out.println(lineCounter-1);
    
}
}






                  
          
 

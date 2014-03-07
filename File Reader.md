Computer-science-OOP
====================

import java.util.Scanner;
import java.io.*;

public class MainOOP{
  public static void main(String args[]) throws Exception{
    int lineCounter = 0;
    try{//tries out the code
      Scanner in = new Scanner(new FileReader("DRUGZZ.txt"));
      String x;
      while((x = in.nextLine()) != null){//reads file line by line until the end
          lineCounter++;
}
    }catch (Exception e){
      if(e.getMessage().equals("No line found")){
        System.out.print("");
      }else{
      System.out.println("There is an error: " + e.getMessage());
     
}
}
    try{//tries out the code
    Scanner in = new Scanner(new FileReader("DRUGZZ.txt"));
    String a;
    String data[][] = new String[lineCounter-1][8];
    System.out.print(lineCounter);
    int c = 0;
    in.nextLine();
    while((a = in.nextLine()) != null){//reads file line by line until the end
      data[c] = a.split(" ");
      c++;
    }
    }catch (Exception e){ 
      if(e.getMessage().equals("No line found")){
        System.out.print("");
      }else{
      System.out.println("There is an error: " + e.getMessage());
   
    
    
}
}
  }
}




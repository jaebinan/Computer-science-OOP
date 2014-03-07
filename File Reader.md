Computer-science-OOP
====================

import java.util.Scanner;
import java.io.*;

public class MainOOP{
  
  public static void main(String args[]) throws IOException{
    int lineCounter = 0;//keeps record of number of lines
    try{//tries out the code
      Scanner in = new Scanner(new FileReader("DRUGZZ.txt"));
      String x;
      while((x = in.nextLine()) != null){//reads file line by line until the end
          lineCounter++;//adds to number of lines
}in.close();//closes file
    }catch (Exception e){//catches exceptions if any
      if(e.getMessage().equals("No line found")){//ignores the error "No line Found"
        System.out.print("");
      }else{  
      System.out.println("There is an error: " + e.getMessage());//outputs the error message
    } 
    }
     
    Scanner in = new Scanner(new FileReader("DRUGZZ.txt"));
    String x;
    String sd;
    String[] lines = new String[lineCounter];;//initialize 1D arrdy 
    sd = in.nextLine();//skips the first line (headings)
    try{
    for (int y=0; y<(lineCounter-1); y++) {//goes through all the rows of the array and lines of the text file
    x = in.nextLine();//reads lines of the text file
    lines[y] = x.trim();
    }
    }catch (Exception e){
      if(e.getMessage().equals("No line found")){//ignores the error "No line Found"
        System.out.print("");
      }else{
      System.out.println("There is an error: " + e.getMessage());//outputs the error message
    } 
    }
      
  Customer d[] = new Customer[lineCounter-1];

  String[] parts = new String[7];
  for(int i = 0; i < (lineCounter-1); i++) {
   parts = lines[i].split(",");
   String dc = (parts[0]);
   String n = (parts[1]);
   double quantm = Double.parseDouble(parts[2]);
   double quantw = Double.parseDouble(parts[3]);
   double rev = Double.parseDouble(parts[4]);
   double pro = Double.parseDouble(parts[5]);
   double salew = Double.parseDouble(parts[6]);
   String dem = (parts[7]);
   d[i] = new Customer(dc, n, quantm, quantw, rev, pro, salew, dem); 

   try{
   if(((parts[4])== null) && ((parts[5])== null)&& ((parts[6])==null)&& ((parts[7])==null)) {
    d[i] = new Customer(dc, n, quantm, quantw);
   } else {
    d[i] = new Customer(dc, n, quantm, quantw, rev, pro, salew, dem);
   }
   }catch (Exception e){
     System.out.println("There is an error: " + e.getMessage());
        
  }
}
  
}
}

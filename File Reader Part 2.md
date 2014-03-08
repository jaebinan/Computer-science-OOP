Computer-science-OOP
==================

import java.util.Scanner;
import java.io.*;

public class MainOOP2{
  
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
    try{//tries code
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
      
  Customer d[] = new Customer[lineCounter-1];//initializes object array with size line counter-1

  String[] parts = new String[7];//initializes a string array 
  for(int i = 0; i < (lineCounter-1); i++) {//forloop that goes through each 
   parts = lines[i].split(",");//declares variables for the object
   String dc = (parts[0]);// Initializes dc
   String n = (parts[1]);// Initializes n
   double quantm = Double.parseDouble(parts[2]); //convert array value to double and set values
   double quantw = Double.parseDouble(parts[3]); //convert array value to double and set values
   double rev = Double.parseDouble(parts[4]); //convert array value to double and set values
   double pro = Double.parseDouble(parts[5]); //convert array value to double and set values
   double salew = Double.parseDouble(parts[6]); //convert array value to double and set values
   String dem = (parts[7]);//initializes dem
   d[i] = new Customer(dc, n, quantm, quantw, rev, pro, salew, dem); //creates an object

   try{//tries code
   if(((parts[4])== null) && ((parts[5])== null)&& ((parts[6])==null)&& ((parts[7])==null)) {//checks which constructor to use
    d[i] = new Customer(dc, n, quantm, quantw);//constructs new object
   } else {
    d[i] = new Customer(dc, n, quantm, quantw, rev, pro, salew, dem);//constructs new object
   }
   }catch (Exception e){//catches exception
     System.out.println("There is an error: " + e.getMessage());//print error message
        
  }
}
  Helper.menu(d);
}
}

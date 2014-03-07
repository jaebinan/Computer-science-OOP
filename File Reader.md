Computer-science-OOP
====================

import java.util.Scanner;
import java.io.*;

public class MainOOP{
  public static void main(String args[]) throws Exception{
    int lineCounter = 0;//keeps record of number of lines
    int col = 0;//keeps record of the number of columns
    try{//tries out the code
      Scanner in = new Scanner(new FileReader("DRUGZZ.txt"));
      String x;
      while((x = in.nextLine()) != null){//reads file line by line until the end
        col = x.split(",").length;//determines the numbers of columns
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
    String[] lines;//initialize 1D arrdy 
    String[][] data = new String[lineCounter][col];//initialize 2D arrdy  
    sd = in.nextLine();//skips the first line (headings)
    try{
    for (int y=0; y<(lineCounter-1); y++) {//goes through all the rows of the array and lines of the text file
    x = in.nextLine();//reads lines of the text file
    lines = x.split(",");
      for(int l = 0; l<lines.length;l++){//goes through all the rows of the array
        data[y][l] = lines[l];//store data into the 2D array         
}
    }
    }catch (Exception e){
      if(e.getMessage().equals("No line found")){//ignores the error "No line Found"
        System.out.print("");
      }else{
      System.out.println("There is an error: " + e.getMessage());//outputs the error message
    } 
    }
      
  drug d[] = new drug[lineCounter-1];
  //String noData = null;


  for(int i = 0; i < (lineCounter-1); i++) {
   
   String dc = (data[i][0]);
   String n = (data[i][1]);
   double quantm = Double.parseDouble(data[i][2]);
   double quantw = Double.parseDouble(data[i][3]);
   double rev = Double.parseDouble(data[i][4]);
   double pro = Double.parseDouble(data[i][5]);
   double salew = Double.parseDouble(data[i][6]);
   String dem = (data[i][7]);
   d[i] = new drug(dc, n, quantm, quantw, rev, pro, salew, dem); 

  
   if(((data[i][4])== null) && ((data[i][5])== null)&& ((data[i][6])==null)&& ((data[i][7])==null)) {
    d[i] = new drug(dc, n, quantm, quantw, rev, pro, salew, dem); 
   } else {
    d[i] = new drug(dc, n, quantm, quantw);
   }
  }
        
  }
}





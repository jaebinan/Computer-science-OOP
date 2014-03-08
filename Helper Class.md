Computer-science-OOP
====================

import java.util.Scanner;
import java.io.*;
import java.util.*;

public class Helper{
  public static Customer[] d;
  public static Scanner in = new Scanner(System.in);
  
  public static void menu(Customer[] a) throws IOException{
    d = a;
    try{//tries out the code
    int i =0;
  
  while(i==0){//while loop to keep asking 
  Scanner in = new Scanner(System.in);
  System.out.println("What would you like to do?");
  System.out.println("A: Display the code of a drug");
  System.out.println("B: Display quantity of the drug in money and weight");
  System.out.println("C: Update quantity of the drug in money and weight");
  System.out.println("D: Display Revenues and Profits of each drug");
  System.out.println("E: Display the production cost of each drug");
  System.out.println("F: Display the demand of each drug");
  System.out.println("G: Update the revenue of the drug");
  System.out.println("Exit: to exit the menu");
  String option = in.nextLine();//promts user for input
  
    if (option.equalsIgnoreCase("a")){//if statement to act on input option
      System.out.println("Please enter the name of the drug");//promt user for name of drug
      String name = in.nextLine();                                                   
      System.out.println(DisplayC(name));//outputs drug code
    }else if(option.equalsIgnoreCase("b")){
      System.out.println("Please enter the name of the drug");//promt user for name of drug
      String name = in.nextLine();                              
      System.out.println(DisplayQuantityMW(name));//outputs drug name
    }else if(option.equalsIgnoreCase("c")){
      System.out.println("Please enter the name of the drug");//promt user for name of drug
      String name = in.nextLine(); 
      System.out.println("Please enter the quantity in money of the drug");//promt user for a new quantity in money value
      double qm = in.nextDouble();
      System.out.println("Please enter the quantity in weight of the drug");//promt user for a new quantity in weight value
      double qw = in.nextDouble();
      updateQuantityMW(name,qm,qw);//updates the quantities
    }else if(option.equalsIgnoreCase("d")){
      System.out.println("Please enter the name of the drug");//promt user for name of drug
      String name = in.nextLine();                           
      System.out.println(DisplayRevProf(name));//outputs the revenue and profit
    }else if(option.equalsIgnoreCase("e")){
      System.out.println("Please enter the name of the drug");//promt user for name of drug
      String name = in.nextLine();                           
      System.out.println(DisplayProdCost(name));//outputs the production cost
    }else if(option.equalsIgnoreCase("f")){
      System.out.println("Please enter the name of the drug");//promt user for name of drug
      String name = in.nextLine();                           
      System.out.println(DisplayDemand(name));//outputs the demand of the drug
    }else if(option.equalsIgnoreCase("g")){
      System.out.println("Please enter the name of the drug");//promt user for name of drug
      String name = in.nextLine();  
      System.out.println("Please enter the updated revenue");//promt user for a new revenue value
      double revenue = in.nextDouble();
      updateRev(name,revenue);//updates the revenue value
    }else if(option.equalsIgnoreCase("exit")){
      i = 1;
    }else {
      System.out.println("Invalid Input");
       
    }
  }
    }catch (Exception e){//catches exceptions
      System.out.println("There was an error: " + e.getMessage());//prints out error message
    }
  }
  /**
   * @Method that displays the drug code
   * @param name the name of the drug
   * return drug code
   */
  public static String DisplayC(String name){
    for(int i = 0; i<d.length;i++){//for loop to go through each array element
    if(d[i].getName().equalsIgnoreCase(name)){//checks each object for the specific name
      return "The code for "+ name+" "+d[i].getDrugCode();
    }
  }
    return "Drug not found";
  }
  /**
   * @Method that displays the quantity of the drug in money and weight
   * @param name the name of the drug
   * return drug code
   */
  public static double DisplayQuantityMW(String name){
     for(int i = 0; i<d.length;i++){//for loop to go through each array element
    if(d[i].getName().equalsIgnoreCase(name)){//checks each object for the specific name
      System.out.println("The quantity in money of "+name+" is "+d[i].getQuantityMoney());
      System.out.print("The quantity in weight of "+name+" is ");
      return d[i].getQuantityWeight();
    }
  }
     return -1;
  }
  /**
   * @Method that displays the revenue and profit of the drug
   * @param name the name of the drug
   * return drug revenue and profit
   */
  public static double DisplayRevProf(String name){
    for(int i = 0; i<d.length;i++){//for loop to go through each array element
    if(d[i].getName().equalsIgnoreCase(name)){//checks each object for the specific name
      System.out.println("The revenue of "+name+" is "+d[i].getRevenue());
      System.out.print("The profit of "+name+" is ");
      return d[i].getProfit();
    }
  }
    return -1;
  }
  /**
   * @Method that displays the production cost of the drug
   * @param name the name of the drug
   * return drug production cost
   */
  public static double DisplayProdCost(String name){
    for(int i = 0; i<d.length;i++){//for loop to go through each array element
    if(d[i].getName().equalsIgnoreCase(name)){//checks each object for the specific name
      System.out.print("The production cost of "+name+" is ");
      return d[i].getCostOfOpperation();
    }
  }
    return -1;
  }
  /**
   * @Method that displays the demand of the drug
   * @param name the name of the drug
   * return drug demand
   */
  public static String DisplayDemand(String name){
    for(int i = 0; i<d.length;i++){//for loop to go through each array element
    if(d[i].getName().equalsIgnoreCase(name)){//checks each object for the specific name
      return "The demand of "+name+" is "+ d[i].getDemand();
    }
  }
    return "Drug not found";
  }
  /**
   * @Method that updates the revenue of a drug
   * @param name the name of the drug
   * @param rev the revenue of the drug
   * return void
   */
  public static void updateRev(String name,double rev){
    for(int i = 0; i<d.length;i++){//for loop to go through each array element
    if(d[i].getName().equalsIgnoreCase(name)){//checks each object for the specific name
      d[i].updateRevenue(rev);
    }
  }
  }
  
   public static int finder(Customer[] d, String id){
    for (int i = 0; i<d.length;i++){//for loop to go through each array element
      if((d[i].getDrugCode()).equalsIgnoreCase(id)){//checks each object for the specific name
        return i;
      }
  }
     return -1;
  }
   
   /**
   * @Method that updates the quantity in money and weight 
   * @param qm quantity in money
   * @param qw quantity in weight
   * return void
   */
  public static void updateQuantityMW(String name,double qm, double qw){
    for (int i = 0; i<d.length;i++){//for loop to go through each array element
      if((d[i].getName()).equalsIgnoreCase(name)){//checks each object for the specific name
        d[i].updateQuantity(qm,qw);

  }
    }
  }
}
   
   

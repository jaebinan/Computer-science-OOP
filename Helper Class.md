Computer-science-OOP
====================

import java.util.Scanner;
import java.io.*;
import java.util.*;

public class Helper{
  public static Customer[] d;
  public static Scanner in = new Scanner(System.in);
  
  public static void menu(Customer[] d) throws IOException{
    try{
    int i =0;
  
  while(i==0){
  Scanner in = new Scanner(System.in);
  System.out.println("What would you like to do?");
  System.out.println("A: Display the code of a drug");
  System.out.println("B: Display quantity of the drug in money and weight");
  System.out.println("C: Display Revenues and Profits of each drug");
  System.out.println("D: Display the production cost of each drug");
  System.out.println("E: Display the demand of each drug");
  System.out.println("F: Display the demand of each drug");
  System.out.println("Exit: to exit the menu");
  String option = in.nextLine();
  
    if (option.equalsIgnoreCase("a")){
      System.out.println("Please enter the name of the drug");
      String name = in.nextLine();                                                   
      System.out.println(DisplayC(name));
    }else if(option.equalsIgnoreCase("b")){
      System.out.println("Please enter the name of the drug");
      String name = in.nextLine();                              
      System.out.println(DisplayQuantityMW(name));
    }else if(option.equalsIgnoreCase("c")){
      System.out.println("Please enter the name of the drug");
      String name = in.nextLine();                           
      System.out.println(DisplayRevProf(name));
    }else if(option.equalsIgnoreCase("d")){
      System.out.println("Please enter the name of the drug");
      String name = in.nextLine();                           
      System.out.println(DisplayProdCost(name));
    }else if(option.equalsIgnoreCase("e")){
      System.out.println("Please enter the name of the drug");
      String name = in.nextLine();                           
      System.out.println(DisplayDemand(name));
    }else if(option.equalsIgnoreCase("exit")){
      i = 1;
    }else {
      System.out.println("Invalid Input");
       
    }
  }
    }catch (Exception e){
      System.out.println("There was an error: " + e.getMessage());
    }
  }
  /**
   * @Method that displays the drug code
   * @param name the name of the drug
   * return drug code
   */
  public static String DisplayC(String name){
    for(int i = 0; i<d.length;i++){
    if(d[i].getName().equalsIgnoreCase(name)){
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
     for(int i = 0; i<d.length;i++){
    if(d[i].getName().equalsIgnoreCase(name)){
      return d[i].getQuantityMoney()+ d[i].getQuantityWeight();
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
    for(int i = 0; i<d.length;i++){
    if(d[i].getName().equalsIgnoreCase(name)){
      return d[i].getRevenue()+d[i].getProfit();
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
    for(int i = 0; i<d.length;i++){
    if(d[i].getName().equalsIgnoreCase(name)){
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
    for(int i = 0; i<d.length;i++){
    if(d[i].getName().equalsIgnoreCase(name)){
      return d[i].getDemand();
    }
  }
    return "Drug not found";
  }
  
   public static int finder(Customer[] d, String id){
    for (int i = 0; i<d.length;i++){
      if((d[i].getDrugCode()).equalsIgnoreCase(id)){
        return i;
      }
  }
     return -1;
  }
   }
   



    

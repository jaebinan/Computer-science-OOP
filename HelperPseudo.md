Computer-science-OOP
====================

import java.util.Scanner;
import java.io.*;
import java.util.*;

public class HelperPseudo{
  initialize public static Customer[] d;
  initialize public static Scanner in = new Scanner(System.in);
  
  public static void menu(Customer[] a) throws Exceptions{
    let d = a;
    try code{
    initialize  int i =0;
  
  while loop for when(i==0){
  create scanner
  Output "What would you like to do?";
  Output "A: Display the code of a drug";
  Output "B: Display quantity of the drug in money and weight";
  Output "C: Update quantity of the drug in money and weight";
  Output "D: Display Revenues and Profits of each drug";
  Output "E: Display the production cost of each drug";
  Output "F: Display the demand of each drug";
  Output "G: Update the revenue of the drug";
  Output "H: Locate the a drug in an array";
  Output "Exit: to exit the menu";
  prompt user for input String option
  
    if statement condition(option equalsIgnoreCase("a")){
      Output "Please enter the name of the drug";
      initialize String name = in.nextLine();                                                   
      Output method DisplayC(name);
    }else if statement condition(option equalsIgnoreCase("b")){
      Output "Please enter the name of the drug";
      initialize String name = in.nextLine();                              
      Output method DisplayQuantityMW(name);
    }else if statement condition(option equalsIgnoreCase("c")){
      Output "Please enter the name of the drug";
      initialize String name = in.nextLine(); 
      Output "Please enter the quantity in money of the drug";
      initialize double qm = in.nextDouble();
      Output "Please enter the quantity in weight of the drug";
      initialize double qw = in.nextDouble();
      use method updateQuantityMW(name,qm,qw);
    }else if statement condition(option equalsIgnoreCase("d")){
      Output "Please enter the name of the drug";
      initialize String name = in.nextLine();                           
      Output method DisplayRevProf(name);
    }else if statement condition(option equalsIgnoreCase("e")){
      Output "Please enter the name of the drug";
      initialize String name = in.nextLine();                           
      Output method DisplayProdCost(name);
    }else if statement condition(option equalsIgnoreCase("f")){
      Output "Please enter the name of the drug";
      initialize String name = in.nextLine();                           
      Output method DisplayDemand(name);
    }else if statement condition(option equalsIgnoreCase("g")){
      Output "Please enter the name of the drug";
      initialize String name = in.nextLine();  
      Output "Please enter the updated revenue";
      initialize double revenue = in.nextDouble();
      use method updateRev(name,revenue);
    }else if statement condition(option equalsIgnoreCase("h")){
      Output "Please enter the code of the drug";
      initialize String id = in.nextLine();
      Output method finder(a,id);
    }else if statement condition(option equalsIgnoreCase("exit")){
      i = 1;
    }else {
      output("Invalid Input");
       
    }
  }
    }catch exceptions{
      output error message
    }
  }
  /**
   * @Method that displays the drug code
   * @param string name the name of the drug
   * return the drug code
   */
  public static String DisplayC(String name){
    for loop condition(int i = 0; i<d.length;i++){
    if statement condition(d[i].getName() equalsIgnoreCase(name)){
      output "The code for "+ name+" "+d[i].getDrugCode();
    }
  }
    return "Drug not found";
  }
  /**
   * @Method that displays the quantity of the drug in money and weight
   * @param string name the name of the drug
   * return drug code
   */
  public static double DisplayQuantityMW(String name){
     for loop condition(int i = 0; i<d.length;i++){
    if statement condition(d[i].getName().equalsIgnoreCase(name)){
      Output "The quantity in money of "+name+" is "+d[i].getQuantityMoney();
      Output "The quantity in weight of "+name+" is ";
      return d[i].getQuantityWeight();
    }
  }
     return -1;
  }
  /**
   * @Method that displays the revenue and profit of the drug
   * @param string name the name of the drug
   * return drug revenue and profit
   */
  public static double DisplayRevProf(String name){
    for loop condition(int i = 0; i<d.length;i++){
    if statement condition(d[i].getName().equalsIgnoreCase(name)){
      Output "The revenue of "+name+" is "+d[i].getRevenue());
      Output "The profit of "+name+" is ");
      return d[i].getProfit();
    }
  }
    return -1;
  }
  /**
   * @Method that displays the production cost of the drug
   * @param string name the name of the drug
   * return drug production cost
   */
  public static double DisplayProdCost(String name){
    for loop condition(int i = 0; i<d.length;i++){
    if statement condition(d[i].getName().equalsIgnoreCase(name)){
      Output "The production cost of "+name+" is ";
      return d[i].getCostOfOpperation();
    }
  }
    return -1;
  }
  /**
   * @Method that displays the demand of the drug
   * @param string name the name of the drug
   * return drug demand
   */
  public static String DisplayDemand(String name){
    for loop condition(int i = 0; i<d.length;i++){
    if statement condition(d[i].getName().equalsIgnoreCase(name)){
      Output "The demand of "+name+" is "+ d[i].getDemand();
    }
  }
    return "Drug not found";
  }
  /**
   * @Method that updates the revenue of a drug
   * @param string name the name of the drug
   * @param double rev the revenue of the drug
   * return void
   */
  public static void updateRev(String name,double rev){
    for loop condition (int i = 0; i<d.length;i++){
    if statement condition(d[i].getName().equalsIgnoreCase(name)){
      d[i].updateRevenue(rev);
    }
  }
  }
  /**
   * @Method that locates 
   * @param string name the name of the drug
   * @param string id the drug code
   * return void
   */
   public static int finder(Customer[] d, String id){
    for loop condition (int i = 0; i<d.length;i++){
      if statement condition(d[i].getDrugCode().equalsIgnoreCase(id){
        Output "Row Number ";
        return i;
      }
  }
     return -1;
  }
   
   /**
   * @Method that updates the quantity in money and weight 
   * @param double qm quantity in money
   * @param double qw quantity in weight
   * return void
   */
  public static void updateQuantityMW(String name,double qm, double qw){
    for loop condition (int i = 0; i<d.length;i++){
      if statement condition d[i].getName().equalsIgnoreCase(name){
        use method d[i].updateQuantity(qm,qw);

  }
    }
  }
}
   
   



    

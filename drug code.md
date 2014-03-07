Computer-science-OOP
====================

public class drug{ 
  private String drugCode;
  private String name;
  private double quantityMoney;
  private double quantityWeight;
  private double revenue;
  private double profit;
  private double salesW;
  private String demand;
  
   /**
   * Constructor for initializing a drug object
   * @param dc drug code 
   * @param n name 
   * @param quantm quantity in money
   * @param quantw quantity in weight
   * @param rev revenue 
   * @param prof profit 
   * @param salew sales in weight
   * @param dem demand
   */ 
   public drug (String dc, String n, double quantm, double quantw, double rev, double prof, double salew, String dem){
    drugCode = dc; 
    name = n;
    quantityMoney = quantm;
    quantityWeight = quantw;
    revenue = rev;
    profit = prof;
    salesW = salew; 
    demand = dem;
  }
  /**
   * Constructor for initializing a drug object
   * @param dc drug code 
   * @param n name 
   * @param quantm quantity in money
   * @param quantw quantity in weight
   */ 
   public drug (String dc, String n, double quantm, double quantw){
    drugCode = dc;
    name = n;
    quantityMoney = quantm;
    quantityWeight = quantw;
    revenue = 0;
    profit = 0;
    salesW = 0; 
    demand = "";
  }
  /**
   * @Method that sets the code of the drug
   * @param the code
   * return void
   */
  protected void setCode(String dc){
    drugCode = dc;
}
   
  /**
   * @Method that sets the name of the drug
   * @param the name
   * return void
   */
  protected void setName(String n){
    name = n;
}
  /**
   * @Method that gets the quantity in money
   * @param quantm the quantity in money
   * return true if successful
   */
  protected boolean setQuantityMoney(double quantm){
    quantityMoney = quantm;
    return true;
}
  /**
   * @Method that gets the quantity in weight in kilograms
   * @param quantm the quantity in weight
   * return true if successful
   */
  protected boolean setQuantityWeight(double quantw){
    quantityWeight = quantw;
    return true;
}
  /**
   * @Method that updates the revenue   
   * @param revenue the revenue in millions
   * return void
   */
  public void updateRevenue(double rev){
    if (rev>100){
      demand = "very high";
    }if(rev>50){
      demand = "high";
  }if(rev>10){
    demand = "medium";
  }if(rev>1){
    demand = "low";
}else{
  demand = "very low";
}
  }
  
  /**
   * @Method that gets the code of the drug
   * return the drug of the drug
   */
  public String getDrugCode(){
    return drugCode;
}

   /**
   * @Method that gets the name of the drug
   * return the name of the drug
   */
  public String getName(){
    return name;
}
  /**
   * @Method that gets the quantity of the drugs in money
   * return the quantity of the drug in money
   */
  public double getQuantityMoney(){ 
    return quantityMoney;
  }
  
   /**
   * @Method that gets the quantity of the drugs in weight
   * return the quantity of the drug in weight
   */
  public double getQuantityWeight(){
    return quantityWeight;
  }
   /**
   * @Method that gets the revenue
   * return the revenue
   */
  public double getRevenue(){
    return revenue;
    
}
  
   /**
   * @Method that gets the profit
   * return the profit
   */
  public double getProfit(){
    return profit;
    
}
   /**
   * @Method that gets the sales in weight
   * return the sales in weight
   */
  public double getSalesw(){
    return salesW;
    
}
   /**
   * @Method that gets the demand
   * return the demand
   */
  public String getDemand(){
    return demand;
    
}
  /**
   * @Method that gets the cost of opperations
   * return the cost of opperations
   */
  public double getCostOfOpperation(){
    double COT = revenue - profit;
    return COT;
  
  
}
}

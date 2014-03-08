Computer-science-OOP
===============
Customer
-DrugCode: String
-name: String
-quantityMoney: double
-quantityWeight: double
-Revenue: double
-profit: double
-salesW: double
-demand: String
+Customer(dc: String, n: String, quantM: double, quantW: double,
	 rev: double, prof: double,salew dem: String)
+Customer(dc: String, n: String, quantM: double, quantW: double)
#setCode(dc: String):void
#setName(n: String):void
#setQuantityMoney(quantM: double):boolean
#setQuantityWeight(quantW: double):Boolean
+updateRevenue(rev: double):void
+updateQuantity(qm: double,qw: double):void
+getDrugCode():String 
+getName():String
+QuantityMoney():double
+QuantityWeight():double
+getPrice():double
+getRevenue():double
+getPrice():double
+getDemand():String

# Bus-Ticket-Booking-System
It's My First Repository


package Student;
import java.util.Scanner;

public class Bus_Ticket_Booking_System 
{	
	     static Scanner sc = new Scanner(System.in);
	   public static void main(String[] args) throws InterruptedException 
	{
		System.out.println( "           ~~~~~~~~~~WELCOME~~~~~~~~~\n"               );
		
		System.out.println("           🎫To The Bus Ticket Booking System🎫");		
            
       System.out.println("Enter Your Name:\n ");
       String name= sc.nextLine();
       int num;
       do 
       {     
       System.out.println("Press 1 For Enter The System: ");
        num = sc.nextInt();
        try
        {
        	if(num!=1) 
        	{
          	  throw new Exception("Wrong Press! Please Again Press 1 For Enter");
            }
        }
        catch(Exception e) 
        {
        	System.out.println(e);
        }
       }
       while(num!=1);
       System.out.println("Hii, "+ name);  
       System.out.println("Create You Account: ");
       System.out.println("Enter Your Name:");
       String name4=sc.next();
       
       System.out.println("Enter Your Age: ");
       int agge = sc.nextInt();
       
       System.out.println("Enter Your Email: ");
       String email = sc.next();
       
       System.out.println("Enter Your Mobile Number: ");
       long mob=sc.nextLong();
       
       System.out.println("Create a password: ");
       String pass1 = sc.next();
       
       System.out.println("Conform Password: ");
       String pass2 = sc.next();
       if(pass1==pass2)
       {
    	   System.out.println("Your Account Has Been Created Successfully Done!\n");
    	   System.out.println("Profile...");
    	   System.out.println("Name-"+name4+"     Agr-"+agge);
    	   System.out.println("Email Address-"+email+"      Contact-"+mob);
    	   System.out.println("Your User ID: ");
    	   
       }
       else
       {
    	   System.out.println("Password Not Matched");
       }
       
    	  	while(true) {
    	  	   	  	
    	int numberofticket;
    	int totaltickets=21;
    	do
    	{      		
    		System.out.println("Tickets Available:");
          System.out.println("How Many Number Of Ticket You Want To Book?? Please Enter:");
          numberofticket= sc.nextInt();                  
          try 
          {       	       
          if(numberofticket<=0) 
          {
        	  throw new Exception("Invalid Choice Number Of Tickets! Please Enter Valid Number:");
          }
          }    	
          catch(Exception e)  
          {
        	  System.out.println(e);
          }
    	}
    	while(numberofticket<=0);
    	 int tickettype;
        	  System.out.println("The Type Of Ticket 'AC' OR 'NON-AC':");

        	  System.out.println("If You Need AC Press: 1");
        	  System.out.println("If You Need NON AC Press: 2");
        	   tickettype= sc.nextInt();     
        	  if(tickettype==1) 
        	  {        	   
        		  System.out.println("You Choose AC  And "+numberofticket+" Ticket");
        		       		  
        		  System.out.println("Enter Your Age: ");
        		  int age = sc.nextInt();
        		  if(age<=5)
        		  {
        			  System.out.println("You Can Free Travel:");        			             		  
            		  System.out.println("Enter Passenger First Name:");
            		  String naam= sc.next();
            		  
            		  System.out.println("Enter Passenger Last Name: ");
            		  String naam2= sc.next();
            		  
            		  System.out.println("From: ");
            		  String From = sc.next();
            		  
            		  System.out.println("TO: ");
            		  String TO = sc.next();
            		  
            		  System.out.println("Please Wait Your Ticket Is Booking Processing...");
            		  for(int j=1; j<=5; j++) 
            		  {
            			  System.out.println(j);
            			  Thread.sleep(1000);
            		  }
            		  int left=totaltickets-numberofticket;
        			  System.out.println("* * * * *CHILD FREE TICKET* * * *  *");
        			  System.out.println("Passenger Name:"+naam+" "+naam2  +" *" );
        			  System.out.println("Age: "+age+"               Total Passengers:"+numberofticket);
        			  System.out.println("From: "+From+"            TO:"+TO+"    *");
        			  System.out.println("Air -Condition(AC)");
        			  System.out.println("Payment: Child Free Travel          *");
        			  System.out.println();
        			  System.out.println("* * * * * *HAPPY JOURNEY* * * * * * *\n");
        			  System.out.println("Total Ticket Left:"+(left)+"\n");
        			 
        			  System.out.println("~~~~~~~~~~Thank For Booking~~~~~~~~~~\n");
         			  System.out.println("~~If You Want To Book Again~~");       			          			  
        		  }        		  
        		  else if(age>5 && age<60)
        		  {
        			  System.out.println("Enter Your First Name:");
        			  String Fname1 = sc.next();  
        			  
        			  System.out.println("Enter Your Last Name:");
        			  String Lname1 = sc.next();
        			  
        			  System.out.println("Enter Your Age:");
        			  int age11 = sc.nextInt();
        			  
        			  System.out.println("From: ");
            		  String From = sc.next();
            		  
            		  System.out.println("TO: ");
            		  String TO = sc.next();
            		  
            		  int pay;
            		   do
            		   {           			   
                		   System.out.println("Enter The Payment: "+numberofticket*800);
                		   pay=sc.nextInt();
                 	 try 
                 		{
                 		if(pay<numberofticket*800)
                 		{ 
              			  throw new Exception(" You Enter Less Amount! Please Enter Valid Amount");
                 		 }            			   
            			   }
                 		catch(Exception e)
                 		  {
                 			System.out.println(e);
                 		  }
            		   }
            		   while(pay<numberofticket*800);
            		   System.out.println("Please Wait Your Tickets  Booking In Progress...");
            		   for(int i = 1; i<=5; i++)
                        {
            			   System.out.println(i);
            			   Thread.sleep(1000);           			   
            		   }
            		   System.out.println("Tickets Are Sucessuffely Booked \n");
        		       System.out.println("* * * * * * * * * *TICKETS* * * * * * * * *");
        		       System.out.println();
        		       System.out.println("Passengr Name:"+Fname1+Lname1 +"    Age:"+age);
        		       System.out.println();
        		       System.out.println("From: "+From+"                To: "+TO);
        		       System.out.println("Air Condition(AC)");
        		       System.out.println("Payment: "+pay+"/- Done"+ "     Total Passenger:"+numberofticket);
        		       System.out.println();
        		       System.out.println("* * * * * * * * *HAPPY JOURNEY* * * * * * * ");
        		       System.out.println("Total Ticket Left:"+(totaltickets-numberofticket)+"\n");
         			  System.out.println("~~~~~~~~~~Thanks For Booking~~~~~~~~~~\n");
         			  System.out.println("~~If You Want To Book Again~~");      			  
        		  }
        		  else if(age>=60)
        		  {
        			  System.out.println("You Are Aged You Get 20% Discount: ");       			  
        			  System.out.println("Enter Your First Name:");
        			  String Fname = sc.next(); 
        			  
        			  System.out.println("Enter Your Last Name:");
        			  String Lname = sc.next();
        			  
        			  System.out.println("Enter Your Age:");
        			  int age1 = sc.nextInt();
        			  
        			  System.out.println("From:");
        			  String From1= sc.next();
        			  
        			  System.out.println("TO:");
        			  String to = sc.next();  
        			  
        			  int pay;
           		   do
           		   {           			   
               		   System.out.println("Enter The Payment: "+numberofticket*800);
               		   pay=sc.nextInt();
               		  
                		  try 
                		  {
                		   if(pay<numberofticket*800)
                			{ 
             		     throw new Exception(" You Enter Less Amount! Please Enter Valid Amount");
                		  }           			   
           			   }
                		  catch(Exception e)
                		  {
                		   System.out.println(e);
                		  }
           		   }
           		   while(pay<numberofticket*800);
           		   double totalamount=pay;
         		   double discount=20;
         		   double discountamount = (discount/100)*pay;
         		   System.out.println("Please Wait Ticket Booking Is Processing...");
         		   for(int k=1; k<=5; k++)
         		   {
         			   System.out.println(k); 
         			   Thread.sleep(1000);
         		   }
           		System.out.println("Tickets Are Sucessuffely Booked \n");
 		       System.out.println("* * * * * * * * * *TICKETS* * * * * * * * *");
 		       System.out.println();
 		       System.out.println("Passengr Name:"+Fname+Lname +" Age:"+age1);
 		       System.out.println();
 		       System.out.println("From: "+From1+"                To: "+to);
 		       System.out.println("Air Condition(AC)");
 		       System.out.println("Payment: "+pay+"/- Done"+ "     Total Passenger:"+numberofticket);
 		       System.out.println("You Get 20% Discount:"+discountamount);
 		       System.out.println("Discount Amount Has Been Sent Your Bank Account  *");
 		       System.out.println();
 		       System.out.println("* * * * * * * * *HAPPY JOURNEY* * * * * * * ");
 		      System.out.println("Total Ticket Left:"+(totaltickets-numberofticket)+"\n");
 			  System.out.println("~~~~~~~~~~Thanks For Booking~~~~~~~~~~\n");
 			  System.out.println("~~If You Want To Book Again~~");

        		  }
        	  }//First if 
        		  else if (tickettype==2)
        	      {       	 
        			  System.out.println("You Choose NON-AC  And "+numberofticket+" Ticket");
        			  System.out.println("Enter Age: ");
            		  int age2 = sc.nextInt();
            		  if(age2<=5)
            		  {
            			  System.out.println("You Can Free Travel:");
            		  System.out.println("Enter Passenger First Name:");
            		  String naam1= sc.next();
            		  
            		  System.out.println("Enter Passenger Last Name: ");
            		  String naam3= sc.next();
            		            			 
            			  System.out.println("Enter Your Age:");
            			  int age11 = sc.nextInt();
            			  
            			  System.out.println("From:");
            			  String From11= sc.next();
            			  
            			  System.out.println("TO:");
            			  String to1 = sc.next();
            			  
                		  System.out.println("Please Wait Your Ticket Is Booking Processing...");
                		  for(int j=1; j<=3; j++) 
                		  {
                			  System.out.println(j);
                			  Thread.sleep(1000);
                		  }
            			  System.out.println("* * * * *CHILD FREE TICKET* * * *  *");
            			  System.out.println();
            			  System.out.println("Passenger Name:"+naam1+" "+naam3  +" *" );
            			  System.out.println("Age: "+age11+"               Total Passengers:"+numberofticket);
            			  System.out.println("From: "+From11+"            TO:"+to1+"    *");
            			  System.out.println("NON-AC Coach ");
            			  System.out.println("Payment: Chile Free Travel          *");
            			  System.out.println();
            			  System.out.println("* * * * * *HAPPY JOURNEY* * * * * * *");
            			  System.out.println("Total Ticket Left:"+(totaltickets-numberofticket)+"\n");
             			  System.out.println("~~~~~~~~~~Thanks For Booking~~~~~~~~~~\n");
             			  System.out.println("~~If You Want To Book Again~~");
            		  }
            		  else if(age2>5 && age2<60)
            		  {
            			  System.out.println("Enter Your First Name:");
            			  String Fname1 = sc.next();  
            			  
            			  System.out.println("Enter Your Last Name:");
            			  String Lname1 = sc.next();
            			  
            			  System.out.println("Enter Your Age:");
            			  int age11 = sc.nextInt();
            			  
            			  System.out.println("From: ");
                		  String From = sc.next();
                		  
                		  System.out.println("TO: ");
                		  String TO = sc.next();
                		   
                		  int pay;
                		   do
                		   {           			   
                    		   System.out.println("Enter The Payment: "+numberofticket*500);
                    		   pay=sc.nextInt();
                     		  try 
                     		  {
                     		 if(pay<numberofticket*500)
                     		 { 
                  			  throw new Exception(" You Enter Less Amount! Please Enter Valid Amount");
                     		  }                			   
                			     }
                     		  catch(Exception e)
                     		  {
                     			  System.out.println(e);
                     		  }
                		   }
                		   while(pay<numberofticket*500);
                		   System.out.println("Please Wait Your Tickets  Booking In Progress...");
                		   for(int i = 1; i<=6; i++)
                            {
                			   System.out.println(i);
                			   Thread.sleep(1000);           			   
                		   }
                		   System.out.println("Tickets Are Sucessuffely Booked \n");
            		       System.out.println("* * * * * * * * * *TICKETS* * * * * * * * *");
            		       System.out.println();
            		       System.out.println("Passengr Name:"+Fname1+Lname1 +" Age:"+age2);
            		       System.out.println();
            		       System.out.println("From: "+From+"                To: "+TO);
            		       System.out.println("Air Condition(AC)");
            		       System.out.println("Payment: "+pay+"/- Done"+ "     Total Passenger:"+numberofticket);
            		       System.out.println();
            		       System.out.println("* * * * * * * * *HAPPY JOURNEY* * * * * * * ");
            		       System.out.println("Total Ticket Left:"+(totaltickets-numberofticket)+"\n");
              			  System.out.println("~~~~~~~~~~Thanks For Booking~~~~~~~~~~\n");
             			  System.out.println("~~If You Want To Book Again~~");

            		  }
            		  else if(age2>=60 && age2<=100)
            		  {
            			  System.out.println("You Are Aged You Get 20% Discount: ");       			  
            			  System.out.println("Enter Your First Name:");
            			  String Fname = sc.next();   
            			  
            			  System.out.println("Enter Your Last Name:");
            			  String Lname = sc.next();
            			  
            			  System.out.println("Enter Your Age:");
            			  int age1 = sc.nextInt();
            			  
            			  System.out.println("From:");
            			  String From1= sc.next();
            			  
            			  System.out.println("TO:");
            			  String to = sc.next();  
            			  
            			  int pay;
               		   do
               		   {           			   
                   		   System.out.println("Enter The Payment: "+numberofticket*500);
                   		   pay=sc.nextInt();               		  
                    		  try 
                    		  {
                    		   if(pay<numberofticket*500)
                    			{ 
                 		     throw new Exception("You Enter Less Amount! Please Enter Valid Amount");
                    		  }           			   
               			   }
                    		  catch(Exception e)
                    		  {
                    		   System.out.println(e);
                    		  }
               		   }
               		   while(pay<numberofticket*500);
               		   double totalamount=pay;
             		   double discount=20;
             		   double discountamount = (discount/100)*pay;
             		   double totaldiscountamount=pay-discountamount;
             		   System.out.println("Please Wait Ticket Booking Is Processing...");
             		   for(int k=1; k<=8; k++)
             		   {
             			   System.out.println(k);
             			   Thread.sleep(2000);
             		   }
               		System.out.println("Tickets Are Sucessuffely Booked \n");
     		       System.out.println("* * * * * * * * * *TICKETS* * * * * * * * *");
     		       System.out.println();
     		       System.out.println("Passengr Name: "+Fname+Lname +"          Age:"+age1);
     		       System.out.println();
     		       System.out.println("From: "+From1+"                To: "+to);
     		       System.out.println("Air Condition(AC)");
     		       System.out.println("Payment: "+pay+"/- Done"+ "     Total Passenger:"+numberofticket);
     		       System.out.println("You Get 20% Discount:"+discountamount);
     		       System.out.println("Discount Amount Has Been Sent Your Bank Account  *");
     		       System.out.println();
     		       System.out.println("* * * * * * * * *HAPPY JOURNEY* * * * * * * ");
     		      System.out.println("Total Ticket Left:"+(totaltickets-numberofticket)+"\n");
     			  System.out.println("~~~~~~~~~~Thanks For Booking~~~~~~~~~~\n");
     			  System.out.println("~~If You Want To Book Again~~");

            		  }
            	      } //first if block          	 
        	     else 
  	          {
  		       System.out.println("Invalid Choice!");
  	            }  
    	  	        }
    	  	
	              }
                 }
             
                

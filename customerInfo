import java.util.ArrayList;
import java.util.Scanner;

public class customerInfo {
   static Scanner userMenuChoice = new Scanner(System.in); //for id and revenue input
   static Scanner userInfo = new Scanner(System.in); //for name input
   static int numOfCustomers = 0; //customer counter



   static ArrayList customerNames = new ArrayList();
   static ArrayList customerID = new ArrayList();
   static  ArrayList customersRevenue = new ArrayList();

    public static void main(String[] args) {
        int userMenuSelection; //user menu number input

        do{
            //Display menu options
            displayMenu();

            //Prompt for menu number
            System.out.println("Enter a number for your selection.");
            userMenuSelection = userMenuChoice.nextInt();

            //Decide number user entered
            switch (userMenuSelection){
                case 1:
                    addMultipleCustomers();
                    break;
                case 2:
                    addSingleCustomer();
                    break;
                case 3:
                    System.out.println(displayCustomers());
                    break;
                case 4:
                    System.out.println(getSpecificData());
                    break;
                case 5:
                    System.out.println(getCustomerTotalRevenue());
                    break;
                case 6:
                    System.out.println("Thanks for using our program.");
                    break;
                default:
                    System.out.println("Enter a valid number: 1-6");
            }


        }while (userMenuSelection != 6);

    }
    //Method to display menu
    public static void displayMenu(){
        //Display menu choices
        System.out.println("Menu");

        System.out.println("1. Add multiple new customers");
        System.out.println("2. Add single new customer");
        System.out.println("3. Display all customers");
        System.out.println("4. Retrieve specific customer's data");
        System.out.println("5. Retrieve customers with total sales based on the range");
        System.out.println("6. Exit");
    }

    //Method to add multiple customers
    public static void addMultipleCustomers() {

        //Prompt user for number of customers
        System.out.println("Enter the number of customers to be loaded");
        numOfCustomers = userMenuChoice.nextInt();

        //Add names, id, and revenue
        for (int customerCounter = 0; customerCounter < numOfCustomers; customerCounter++) {
            System.out.print("Please enter a name: ");
            String name = userInfo.nextLine();

            customerNames.add(name); //Add name info to array

            System.out.print("Enter a 5 digit ID: ");
            int id = userMenuChoice.nextInt();

            customerID.add(id); //Add id info to array

            Scanner customerRevenue = new Scanner(System.in);
            System.out.print("Total Revenue (as a whole number): ");
            int revenue = customerRevenue.nextInt();

            customersRevenue.add(revenue); //Add revenue info to array
        }
    }

    //Method for single customer
    public static void addSingleCustomer(){
            //Add name, id, and revenue
            System.out.print("Please enter a name: ");
            String name = userInfo.nextLine();

            customerNames.add(name); //Add name info to array

            System.out.print("Enter a 5 digit ID: ");
            int id = userMenuChoice.nextInt();

            customerID.add(id); //Add id info to array

            Scanner customerRevenue = new Scanner(System.in);
            System.out.print("Enter the total revenue (as a whole number): ");
            int revenue = customerRevenue.nextInt();

            customersRevenue.add(revenue); //Add revenue info to array
    }

    //Method display all customers
    public static String displayCustomers(){
        System.out.println("All Customers");
        int infoCounter = 0; //customer info counter
        int customerIDs; //get customer id
        int totalRevenue; //get customer revenue

        while (infoCounter < customerNames.size()){
            String name = (String) customerNames.get(infoCounter);
            customerIDs = (int) customerID.get(infoCounter);
            totalRevenue = (int) customersRevenue.get(infoCounter);

            System.out.printf("Customer's name, id, and revenue: %s %d %d %n", name , customerIDs , totalRevenue); //display all customer info

            infoCounter++;
        }
        return "";
    }

    //Method to retrieve specific customer's data
    public static String getSpecificData(){
        System.out.println("Enter the customer id you'd like to search");
        int userIDSearch = userMenuChoice.nextInt();
        int specificDate = customerID.indexOf(userIDSearch);

        return "Customer Data Lookup (Name, ID, and Revenue): " + customerNames.get(specificDate) + " " + customerID.get(specificDate) + " " + customersRevenue.get(specificDate);
    }

    //Method to retrieve customers with highest and lowest value
    public static String getCustomerTotalRevenue() {
        //Prompt for highest revenue value
        System.out.println("Enter the Highest Total Revenue: ");
        int highestRevenue = userMenuChoice.nextInt();
        int highestRevenueSearch = customersRevenue.indexOf(highestRevenue);

        //Prompt for lowest revenue value
        System.out.println("Enter the Lowest Total Revenue: ");
        int lowestRevenue = userMenuChoice.nextInt();
        int lowestRevenueSearch = customersRevenue.indexOf(lowestRevenue);

        return "Customers with the lowest revenue " + customerNames.get(lowestRevenueSearch) + " and the highest " + customerNames.get(highestRevenueSearch);
        }
}

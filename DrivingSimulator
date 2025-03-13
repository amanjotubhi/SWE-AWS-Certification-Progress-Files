import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

        // TODO 1: Declare the necessary variables for the car's state and add scanner object
        boolean isEngineOn = false;
        String gear = "P";
        int speed = 0;
        int choice = 0;
        Scanner keyBoard = new Scanner(System.in);

        while(choice != 5) {
            // TODO 2: Display the current state of the car (engine state, gear, speed)
            String engineStatus = "";
            if (isEngineOn) {
                engineStatus = "ON";
            } else {
                engineStatus = "OFF";
            }
            System.out.println("\n------Car Dashboard Status -------");
            System.out.println("Engine Status: " + engineStatus);
            System.out.println("Current Gear : " + gear);
            System.out.println("Speed : " + speed + " mph.");

            // TODO 3: Add print statements for each variable you want to display or options available to the user
            System.out.println("\n-------Menu:------------");
            System.out.println("1. Turn on/off the engine");
            System.out.println("2. Change gear (P, D, R)");
            System.out.println("3. Accelerate");
            System.out.println("4. Brake");
            System.out.println("5. Exit");

            // TODO 4: Prompt the user for their choice and store it in the 'choice' variable
            System.out.println("Enter your choice (Number between 1 - 5): ");
            choice = keyBoard.nextInt();
            if (choice < 1 || choice > 5) {
                System.out.println("Invalid user input!");
            } else {
                System.out.println("You choose: " + choice);
            }


            // TODO 5: Implement a switch statement to handle the different menu choices
            switch (choice) {
                case 1:
                    isEngineOn = !isEngineOn;
                    break;
                case 2:
                    System.out.println("Enter gear (P, D, R): ");
                    gear = keyBoard.next();
                    break;
                case 3:
                    if (isEngineOn && !gear.equals("P")) {
                        speed += 10; //increment speed by 10
                    } else {
                        System.out.println("Cannot accelerate while engine is off or in Park (P) gear.");
                    }
                    break;
                case 4:
                    if ((isEngineOn && gear.equals("D")) || (isEngineOn && gear.equals("R"))) {
                        if(speed == 0) {
                            speed = 0;
                        } else {
                            speed -= 10;
                        }
                    } else {
                        System.out.println("Brake is press! You are still in \"P\" gear.");
                    }
            }
        }
        // TODO 6: Make sure the program runs until the user decides it's time to stop. Consider enclosing TODO 2 -> TODO 5 above in a while loop!
        //Done, enclosed it in while loop

    }
}

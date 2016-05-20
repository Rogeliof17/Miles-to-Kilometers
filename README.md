# Miles-to-Kilometers
this program converts miles to kilometers



import javax.swing.JOptionPane;

public class MilesToKilometers {

    public static void main(String[] args) {

        double miles;
        double kilometers;

        //get miles
        miles = getMiles();

        //convert miles to kilometers
        kilometers = MilesToK(miles);

        //display the result
        displayRes(miles, kilometers);

        System.exit(0);

    }

    //method to ask user to input miles for conversion
    public static double getMiles() {

        String input;
        double numMiles;

        //ask user for number of miles
        input = JOptionPane.showInputDialog("This program converts miles to kilometers." +
                "\n Enter the number of miles. ");

        numMiles = Double.parseDouble(input);

        return numMiles;
    }

    //method to calculate conversion
    public static double MilesToK(double numMiles) {

        //convert miles to kilometers and return
        return numMiles * 1.609;

    }

    //method to display kilometers
    public static void displayRes(double miles, double kilometers) {

        JOptionPane.showMessageDialog(null, miles + " is equal to " +
                kilometers + " kilometers. ");
    }
}

# AP-assignment-5th-
Create a constructor class in both base and derived class use super()  to call base class constructor
public class Calculator {
    private String name;

    // Constructor for Calculator
    public Calculator(String name) {
        this.name = name;
        System.out.println("Calculator constructor called: " + name);
    }

    public int add(int a, int b) {
        return a + b;
    }
}
public class AdvancedCalculator extends Calculator {
    private String type;

    // Constructor for AdvancedCalculator
    public AdvancedCalculator(String name, String type) {
        super(name); // Call to the base class constructor
        this.type = type;
        System.out.println("AdvancedCalculator constructor called: " + type);
    }

    public int multiply(int a, int b) {
        return a * b;
    }
}
public class Main {
    public static void main(String[] args) {
        // Create an instance of AdvancedCalculator
        AdvancedCalculator advancedCalculator = new AdvancedCalculator("Basic Calculator", "Scientific");

        // Use the add method from the base class
        int sum = advancedCalculator.add(5, 3);
        System.out.println("Sum: " + sum);

        // Use the multiply method from the derived class
        int product = advancedCalculator.multiply(5, 3);
        System.out.println("Product: " + product);
    }
}

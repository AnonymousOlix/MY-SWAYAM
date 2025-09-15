# Programming In Java

# Week 8

# Programming Assignment 1

```bash
// Declare a 5x5 2D array to store the input
        int[][] matrix = new int[5][5];
        
        // Input 2D Array using Scanner Class and check data validity
        for (int i = 0; i < 5; i++) {
            String row = sc.next();
            if (row.length() != 5 || !row.matches("[01]{5}")) {
                i--;  // Decrement to repeat the current row input
                continue;
            }
            for (int j = 0; j < 5; j++) {
                matrix[i][j] = row.charAt(j) - '0';  // Convert char to int
            }
        }

        // Perform the Flip-Flop Operation (0 to 1 and 1 to 0)
        for (int i = 0; i < 5; i++) {
            for (int j = 0; j < 5; j++) {
                matrix[i][j] = (matrix[i][j] == 0) ? 1 : 0;
            }
        }

        // Output the 2D Flip-Flop Array
        for (int i = 0; i < 5; i++) {
            for (int j = 0; j < 5; j++) {
                System.out.print(matrix[i][j]);
            }
            System.out.println();
        }

        // Close the scanner object
        sc.close();

```

# Programming Assignment 2

```bash
// Declare variables for the operands and operator
        double operand1 = 0, operand2 = 0, result = 0;
        char operator = ' ';

        // Find the operator position and extract operands
        if (input.contains("+")) {
            operator = '+';
            String[] parts = input.split("\\+");
            operand1 = Integer.parseInt(parts[0].trim());
            operand2 = Integer.parseInt(parts[1].trim());
        } else if (input.contains("-")) {
            operator = '-';
            String[] parts = input.split("-");
            operand1 = Integer.parseInt(parts[0].trim());
            operand2 = Integer.parseInt(parts[1].trim());
        } else if (input.contains("*")) {
            operator = '*';
            String[] parts = input.split("\\*");
            operand1 = Integer.parseInt(parts[0].trim());
            operand2 = Integer.parseInt(parts[1].trim());
        } else if (input.contains("/")) {
            operator = '/';
            String[] parts = input.split("/");
            operand1 = Integer.parseInt(parts[0].trim());
            operand2 = Integer.parseInt(parts[1].trim());
        }

        // Perform the operation
        switch (operator) {
            case '+':
                result = operand1 + operand2;
                break;
            case '-':
                result = operand1 - operand2;
                break;
            case '*':
                result = operand1 * operand2;
                break;
            case '/':
                if (operand2 != 0) {
                    result = operand1 / operand2;
                } else {
                    System.out.println("Error: Division by zero");
                    return; // Exit if division by zero
                }
                break;
            default:
                System.out.println("Invalid operation");
                return;
        }

        // Round the result and print in the required format
        result = Math.round(result);  // Round the result
        System.out.println(input + " = " + (long) result);  // Output the result
```

# Programming Assignment 3

```bash
// Constructor to initialize begin and end
    public SquareThread(int begin, int end) {
        this.begin = begin;
        this.end = end;
    }

    // The run method that calculates and prints squares
    @Override
    public synchronized void run() {
        // If begin is greater than end, print in reverse order
        if (begin > end) {
            for (int i = begin; i >= end; i--) {
                System.out.println(i * i);
            }
        } else {
            // Print in ascending order
            for (int i = begin; i <= end; i++) {
                System.out.println(i * i);
            }
        }
    }
```

# Programming Assignment 4

```bash
try {
            // Set up the reader to take input from the user
            InputStreamReader r = new InputStreamReader(System.in);  
            BufferedReader br = new BufferedReader(r);  
            
            // Read the input as a string
            String number = br.readLine();  
            
            // Try to parse the input string into an integer
            int x = Integer.parseInt(number);
            
            // Print the square of the number
            System.out.println(x * x);
        } catch (NumberFormatException e) {
            // If an exception occurs, print the error message
            System.out.println("Please enter valid data");
        } catch (IOException e) {
            // Catch any other I/O errors that might occur
            System.out.println("Error reading input");
        }
```

# Programming Assignment 5

```bash
class Point {
    private double x;
    private double y;

    // Constructor to initialize the coordinates
    public Point(double x, double y) {
        this.x = x;
        this.y = y;
    }

    // Method to calculate the distance between this point and another point
    public double distance(Point p2) {
        double dx = this.x - p2.x; // Difference in x-coordinates
        double dy = this.y - p2.y; // Difference in y-coordinates
        return Math.sqrt(dx * dx + dy * dy); // Euclidean distance formula
    }
}
```


### Congratulations 🎉 You Completed Assignment !

##### *You Have Successfully Demonstrated Your Skills And Determination.*

#### *Well done!*

# [MY SWAYAM](https://www.youtube.com/@MySwayam)

# ParkSlot
Introduction to Parallel Array

```java
import java.io.*;
import java.util.*;

public class Solution {
    //sets the maximum number of elements in each array
    public static final int MAX = 100;
    //sets the counter that determines the last inserted index of the array
    public static int counter = 0;
    
    //declares and iniatilizes the five (5) Park Slot Parallel Array
    public static int[] park_space_id = new int[MAX];
    public static String[] park_vehicle_plate_number = new String[MAX];
    public static boolean[] park_space_status = new boolean[MAX];
    public static String[] park_time_in = new String[MAX];
    public static String[] park_time_out = new String[MAX];    
    
    public static void main(String [] args){
        Scanner input = new Scanner(System.in);
        
        //reads the total number of test cases
        int T = input.nextInt();
        
        //loops the scanned input and assign it to its respective array
        while(counter<T){   
            //scans and stores the next integer to temporary storage
            int user_input_park_space_id = input.nextInt();        
            
            //sets the input scanner to fetch the next strings in the line
            input.nextLine(); 
            String user_input_park_vehicle_plate_number = input.nextLine();
            
            //scans and stores the next boolean to temporary storage
            boolean user_input_park_space_status = input.nextBoolean(); 
            
            //Since the input scanner previously fetched boolean so we will set it back to fetch next strings in a line
            input.nextLine(); 
            String user_input_park_time_in = input.nextLine();            
            String user_input_park_time_out = input.nextLine();
            
            //stores FROM temporary storage TO parallel array
            park_space_id[counter] = user_input_park_space_id;
            park_vehicle_plate_number[counter] = user_input_park_vehicle_plate_number;
            park_space_status[counter] = user_input_park_space_status;
            park_time_in[counter] = user_input_park_time_in;
            park_time_out[counter] = user_input_park_time_out;    
            
            //updates the counter to point the index to the next element in the array
            counter++;
        }
        
        //displays the output of this challenge
        for(int index=0; index<counter; index++){
            System.out.println("PARK SPACE ID: " + park_space_id[index]);
            //Write your codes here...            
        }
    }
}
/*
SAMPLE INPUT:
3
100
NO VALUE 
false
NO VALUE
NO VALUE
999
AAA 123
true
SEPTEMBER 24, 2018, 10AM
NO VALUE
100
ABB 444
true
SEPTEMBER 24, 2018, 11AM
SEPTEMBER 24, 2018, 5PM

SAMPLE OUTPUT:
PARK SPACE ID: 100
PARK VEHICLE PLATE NUMBER: NO VALUE
PARK SPACE STATUS: false
PARK TIME IN: NO VALUE
PARK TIME OUT: NO VALUE

PARK SPACE ID: 999
PARK VEHICLE PLATE NUMBER: AAA 123
PARK SPACE STATUS: true
PARK TIME IN: SEPTEMBER 24, 2018, 10AM
PARK TIME OUT: NO VALUE

PARK SPACE ID: 100
PARK VEHICLE PLATE NUMBER: ABB 444
PARK SPACE STATUS: true
PARK TIME IN: SEPTEMBER 24, 2018, 11AM
PARK TIME OUT: SEPTEMBER 24, 2018, 5PM
*/

```

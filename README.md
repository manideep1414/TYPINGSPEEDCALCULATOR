# TYPINGSPEEDCALCULATOR
The Java Project
import java.time.LocalTime;
	import java.util.Random;	
	import java.util.Scanner;
	import java.util.concurrent.TimeUnit;


	public class ABC {
		static String[] words = {"Internship", "Trees", "Plants", "College", "Laptop", "Coding","Java", "Desktop", "Administration", "Syntax"};

		public static void main(String[] args) throws InterruptedException  {
			
			//We start the program by starting the timer 
			
	          System.out.println("Get");
	          TimeUnit.SECONDS.sleep(1);
	  
	          System.out.println("Set");
	          TimeUnit.SECONDS.sleep(1);
	          
	          System.out.println("GO!!");
	          TimeUnit.SECONDS.sleep(1);
	          
	        //We print the given words at the string
	          Random rand = new Random();
	          for(int i=0;i<10;i++) {
	          System.out.print(words[rand.nextInt(9)] + " ");
	          }
	          System.out.println();
	          
	         
	          double start = LocalTime.now().toNanoOfDay(); //We start the time for typing
	          
	          Scanner scan = new Scanner(System.in);
	          String typedWords = scan.nextLine();
	          
	          double end = LocalTime.now().toNanoOfDay();//The time ends here
	          double elapsedTime = end - start;//The time elapsed is calculated
	          double seconds = elapsedTime / 1000000000.0;//Converts the given time in seconds
	          int numChars = typedWords.length();
	          //The formula for Words per  Minute is (x words / 5) / 1min = y WPM
	          int wpm = (int) ((((double) numChars / 5) / seconds) * 60);
	          //The formula for Characters per Minute is (x characters / seconds) * 60)
	          int cpm = (int) (((double) numChars / seconds) * 60);
	        		  
	          System.out.println("Your typing speed is " + wpm + " wpm !!!!!");
	          System.out.println("You have a speed of " + cpm + " cpm !!!!");
	            if (wpm>80) {
	            		System.out.println("You have a great typing speed!!!");
	            	}
	            if(wpm>45&&wpm<80){
	            		System.out.println("You have a good typing speed!!");
	            	} 
	            else {
	            		System.out.println("You have a normal typing speed!");
	        		
	            	}
		}

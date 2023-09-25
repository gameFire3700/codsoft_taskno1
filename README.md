mport java.util.Random;
import  java.util.Scanner;


public class RandomNumberGuess{

	public static void main(String[] args) {
		// TODO Auto-generated method stub
           Scanner scan = new Scanner(System.in);
           System.out.println("What is your name?");
           String name =scan.nextLine();
           
           System.out.println("Well, "  + name + ", I am thinking of a number between 1 to 20!");
           int myNumber = getRandomNumber(1, 21);
           
           for (int i=0;i<6;i++) {
        	     
        	    Scanner scan2 =new Scanner(System.in);
        	    System.out.println("take a guess. ");
        	    int yourGuess =scan2.nextInt();
        	    
        	    if(yourGuess ==myNumber) {
        	    	 System.out.println("You guessed correctly!");
        	    	 break;
        	    }
        	    else if(yourGuess < myNumber) {
        	    	 // if the user guessed lower than the number
        	    	System.out.println("yoour guess is tooo low");
        	    }
        	    else if(yourGuess> myNumber) {
        	    	  System.out.println("Your guess is too high;");
        	    }
        	    if(i>=5) {
        	    	// if the user gets the answer wrong too many times
        	    	System.out.println();
        	    	System.out.println("Nope. the number I was thinking of was  " +myNumber + "!");
        	    	
        	    }
           }
	}
	
	
	   public static int getRandomNumber(int min, int max) {
		 
		    Random random=new Random();
		    return random.ints(min,max).findFirst().getAsInt();	   
		    
	   }
	
}



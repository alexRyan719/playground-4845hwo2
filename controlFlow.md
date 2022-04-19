# Control Flow

    public static char grade(int score) {
        
        if(score >= 90) {
            return 'A';
        }
        else if(score >= 80) {
            return 'B';
        }
        else if(score >= 70) {
            return 'C';
        }
        else if(score >= 60) {
            return 'D';
        }
        else{
            return 'F';
        }

    }


# Switch 

Switch statements take an input and compare that with different "cases." Depending on which case the input matches, different lines of code will execute. 
The keyword "break" is used to make sure that only those lines are executed. If you want multiple cases to execute, simply remove the keyword "break." Notice
there are a couple break statements commented out already. 

    public class lessSimpleSwitch {

	public static String returnMonth(int numMonth) {
		
		String month = "";
		
		switch(numMonth) {
			case(1):
				month = "January";
				break;
			case(2):
				month = "February";
				break;
			case(3):
				month = "March";
				break;
			case(4):
				month = "April";
				break;
			case(5):
				month = "May";
				break;
			case(6):
				month = "June";
				//break;
			case(7):
				month += "July";
				//break;
			case(8):
				month += "August";
				break;
			case(9):
				month = "September";
				break;
			case(10):
				month = "October";
				break;
			case(11):
				month = "November";
				break;
			case(12):
				month = "December";
				break;
		
		}
		
		return month;
	}
	
	public static void main(String[] args) {
		String test1 = new String(returnMonth(7));
		System.out.println(test1);
		

	}

}

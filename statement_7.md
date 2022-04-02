# Switch Statement Algorithm


    // Helper method to get an int value from a char.
	public static int fromChar(char letter) {
		
		int returnInt = 0;
		
		switch(letter) {
			case 'a':
				returnInt = 1;
				break;
			case 'b':
				returnInt = 2;
				break;
			case 'c':
				returnInt = 3;
				break;
			case 'd':
				returnInt = 4;
				break;
			case 'e':
				returnInt = 5;
				break;
			case 'f':
				returnInt = 6;
				break;
			case 'g':
				returnInt = 7;
				break;
			case 'h':
				returnInt = 8;
				break;
			case 'i':
				returnInt = 9;
				break;
			case 'j':
				returnInt = 10;
				break;
			case 'k':
				returnInt = 11;
				break;
			case 'l':
				returnInt = 12;
				break;
			case 'm':
				returnInt = 13;
				break;
			case 'n':
				returnInt = 14;
				break;
			case 'o':
				returnInt = 15;
				break;
			case 'p':
				returnInt = 16;
				break;
			case 'q':
				returnInt = 17;
				break;
			case 'r':
				returnInt = 18;
				break;
			case 's':
				returnInt = 19;
				break;
			case 't':
				returnInt = 20;
				break;
			case 'u':
				returnInt = 21;
				break;
			case 'v':
				returnInt = 22;
				break;
			case 'w':
				returnInt = 23;
				break;
			case 'x':
				returnInt = 24;
				break;
			case 'y':
				returnInt = 25;
				break;
			case 'z':
				returnInt = 26;
				break;
			default:
				returnInt = -1000;
		}
		
		return returnInt;
	}
	
	// Helper method to get a char from an int value.
	public static char fromInt(int value) {
		
		char returnChar = ' ';
		
		switch(value) {
			case 1:
				returnChar = 'a';
				break;
			case 2:
				returnChar = 'b';
				break;
			case 3:
				returnChar = 'c';
				break;
			case 4:
				returnChar = 'd';
				break;
			case 5:
				returnChar = 'e';
				break;
			case 6:
				returnChar = 'f';
				break;
			case 7:
				returnChar = 'g';
				break;
			case 8:
				returnChar = 'h';
				break;
			case 9:
				returnChar = 'i';
				break;
			case 10:
				returnChar = 'j';
				break;
			case 11:
				returnChar = 'k';
				break;
			case 12:
				returnChar = 'l';
				break;
			case 13:
				returnChar = 'm';
				break;
			case 14:
				returnChar = 'n';
				break;
			case 15:
				returnChar = 'o';
				break;
			case 16:
				returnChar = 'p';
				break;
			case 17:
				returnChar = 'q';
				break;
			case 18:
				returnChar = 'r';
				break;
			case 19:
				returnChar = 's';
				break;
			case 20:
				returnChar = 't';
				break;
			case 21:
				returnChar = 'u';
				break;
			case 22:
				returnChar = 'v';
				break;
			case 23:
				returnChar = 'w';
				break;
			case 24:
				returnChar = 'x';
				break;
			case 25:
				returnChar = 'y';
				break;
			case 26:
				returnChar = 'z';
				break;
			default:
				returnChar = '@';
		}
		
		return returnChar;
	}
	
	// Actual ROT13 encryption method.
	public static String encrypt(String plainText) {
		
		// Declare variables to be used in the encryption process.
		String cipherText = "";
		char newChar = ' ';
		int charVal = 0;
		char currentChar = ' ';
		boolean isUpperCase = false;
		
		// Loop through each char in plainText and calculate the encrypted char.
		for(int i = 0; i < plainText.length();i++) {
			currentChar = plainText.charAt(i);
			
			// Check to see if the char is capitalized. 
			// Set the boolean variable to true if it is.
			if(Character.isUpperCase(currentChar)) {
				isUpperCase = true;
				currentChar = Character.toLowerCase(currentChar);
			}
			
			// Calculate the int value for the new char.
			charVal = fromChar(currentChar) + 13;
			//System.out.println(currentChar);
			//System.out.println("charVal: " + charVal);
			
			// If the new value is higher than 26, or higher than our alphabet,
			// adjust it to be circular.
			// By circular, I mean wrap the sequence around and start back at 
			// the beginning.
			if(charVal > 26) {
				charVal = charVal - 26;
			}

			//System.out.println("charVal is now: " + charVal);

			
			// Calculate the corresponding char from the int value. 
			// If char is non alpha, no change is needed.
			if(charVal < 0) {
				newChar = currentChar;
			} else {
				newChar = fromInt(charVal);
			}
			
			// If the plain text char was upper case, make the cipher 
			// text char upper case as well.
			if(isUpperCase) {
				cipherText += Character.toUpperCase(newChar);
			} else {
				cipherText += newChar;
			}
			isUpperCase = false;
		}
		
		// Return the cipherText produced from the plainText.
		return cipherText;
	}
	
	public static void main(String[] args) {
		String test = encrypt("This is A NEW test, let's see how this works. Low and HiGh abcdefghijklmnopqrstuvwxyz!?()");
		System.out.println(test);
		String test2 = encrypt("Guvf vf N ARJ grfg, yrg'f frr ubj guvf jbexf. Ybj naq UvTu nopqrstuvwxyzabcdefghijkym!?()");
		System.out.println(test2);
	}


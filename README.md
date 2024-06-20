# Roulette
The purpose of this repository is to learn how to use GitHub using Program08 from CS250 taken Spring 2024. Program 08 was designed to allow a single user to play roulette.

## CS 250:Program 08
Main topics: Loop Statements
Library Methods User Defined Methods

## Program Specification: Write a Java program that allows the user to play roulette. In our version of roulette, the roulette wheel has the following characteristics:
• Slots are numbered from 0 to 36
• Even numbered slots (except 0) are colored Red
• Odd numbered slots are colored Black
• The 0 slot is colored Green

The user starts with 100 chips, and each round can place one the following two types of bets - or quit (cash out):
• Bet on a specific number [1, 36] (payout is 35:1)
• Bet on either Red or Black color (payout is 1:1)
• Cash out

## Your program should behave as follows:
• Display a welcome message
• Repeatedly do the following:
  – Ask the user to choose a bet type (or cash out) if number bet or color bet
    ∗ · If number bet : Ask the user for the number to bet on
      · If color bet : Ask the user for color to bet on
    ∗ Ask the user to choose an amount to bet (between 1 chip and the total number of chips the user currently has), and record the bet amount
    ∗ Spin the wheel and report the number and color
    ∗ Inform the use of their win/loss status, and updated the user’s chip total appropriately Until the user chooses to cash out or has no more chips left to bet
• Once the user chooses to cash out a final report is displayed indicating the user’s winnings or loses (relative to their starting with 100 chips).

## Rules and Requirements:
• All user input must be validated
• Given the following method heading, you must write the corresponding definition for a void return method that displays a welcome message containing the bet types and payouts to the screen.
public static void welcome()
• Given the following method heading, you must write the corresponding definition for a int return method that displays a menu and reads, validates, and returns the user’s choice to place a specific bet type or cash out.
public static int getMenuChoice(Scanner stdIn)
• Given the following method heading, you must write the corresponding definition for a int return method that reads, validates, and returns a number to bet on, which must be between 1 and 36.
public static int getNumber(Scanner stdIn)
• Given the following method heading, you must write the corresponding definition for a String return method that reads, validates, and returns a color to bet on, which must be "Red" or "Black".
public static String getColor(Scanner stdIn)
• Given the following method heading, you must write the corresponding definition for a int return method that takes the number of chips the user currently has: chipsNow as its only input. Then reads, validates, and returns a bet amount, which must be between 1 and chipsNow.
public static int getBet(Scanner stdIn, int chipsNow)
• Given the following method heading, you must write the corresponding definition for a String return method that takes the number just spun on the wheel : spinNum as its only input. Then determines and returns the spin color based on spinNum. i.e. "Red", "Black", or "Green"
public static String determineColor(int spinNum)
• Given the following method heading, you must write the corresponding definition for a void return method that takes the number of chips the user currently has: chipsNow as its only input. Then displays the user’s winnings or loses (relative to their starting with 100 chips) to the screen.
public static void report(int chipsNow)

## Notes and Tips:
• Assuming number is an int variable, the following expression will evaluate to true if number is even: (number % 2 == 0)
• No input validation should take place in the main method.
• Try a bottom-up approach, in which you first implement all of the non-main methods, and then provide an implementation for the main method.
• It may be helpful to implement a single wheel spin first, and then allow the user to play multiple spins next.

### Sample run(s):
\$$$$$$$$$$$$$$$$$$$$$$$$$$$$\
    WELCOME TO ROULETTE
\$$$$$$$$$$$$$$$$$$$$$$$$$$$$\
  NUMBER BETS PAYOUT: 35:1
   COLOR BETS PAYOUT: 1:1
\$$$$$$$$$$$$$$$$$$$$$$$$$$$$\
You have 100 chips

1. Pick a number to bet on
2. Pick a color to bet on
3. Cash out

Enter a choice [1-3]: 0
Enter a choice [1-3]: 4
Enter a choice [1-3]: 1

Enter the number to bet on [1-36]: -1
Enter the number to bet on [1-36]: 37
Enter the number to bet on [1-36]: 0

Enter the number of chips to bet [1-100]: 0
Enter the number of chips to bet [1-100]: 101
Enter the number of chips to bet [1-100]: 5

Spinng the wheel ...
Spin number: 31
Spin color : Black
Sorry, you lost
You now have 95 chips

1. Pick a number to bet on
2. Pick a color to bet on
3. Cash out

Enter a choice [1-3]: 2

Enter the color to bet on [Red or Black]: umm
Enter the color to bet on [Red or Black]: red

Enter the number of chips to bet [1-95]: 50

Spinng the wheel ...
Spin number: 16
Spin color: Red
Congrats, you won!
You now have 145 chips

1. Pick a number to bet on
2. Pick a color to bet on
3. Cash out

Enter a choice [1-3]: 3

Thanks for playing, you won a total of 45 chips

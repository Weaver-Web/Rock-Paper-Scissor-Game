# Rock-Paper-Scissor-Game
     
Based on the rules we will construct our game.

import java.util.*;
import java.util.Scanner; 
import java.util.Random; 

public class RockPaperSci {
    public static final String ROCK = "ROCK";
    public static final String PAPER = "PAPER";
    public static final String SCISSORS = "SCISSORS";
	
	public static String getplayM() {
	Scanner sc =new Scanner(System.in);
	String input =sc.next();
	String playerMove =input.toUpperCase();
	return playerMove;
	}
public static String getCm() {
	String cM = null;
	Random random = new Random();
	int input = random.nextInt(3)+1;
	if(input == 1)
		cM= RockPaperSci.ROCK;
	if(input == 2)
		cM= RockPaperSci.PAPER;
	if(input == 3)
		cM= RockPaperSci.SCISSORS;
	return cM;
}

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		System.out.println("ROCK =1\n PAPER =2\n SCISSORS =3\n");
				System.out.println("Enter your input:");
		String computerMove = getCm();
		String playerMove = getplayM();
		if(computerMove.equals(playerMove)) {
			System.out.println("Game is Tie!!");
		}
		else if(playerMove.equals(RockPaperSci.ROCK)) {
			System.out.println(computerMove.equals(RockPaperSci.PAPER)? "Computer wins!":"Player won!");
		}
		else if(playerMove.equals(RockPaperSci.PAPER)) {
			System.out.println(computerMove.equals(RockPaperSci.SCISSORS)? "Computer wins!":"Player won!");
		}
		else {
			System.out.println(computerMove.equals(RockPaperSci.ROCK)? "Computer wins!":"Player won!");
		}
	}

}

             

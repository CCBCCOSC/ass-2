ass-2
=====

chapter 10
import java.util.Scanner;
public class Quiz

{
private int score;
private Question[] questionHolder = new Question[25];
private int numQuestions;



public Quiz()
{
this.score = 0;
this.numQuestions = 0;

}

public void addQuestion (Question Q)
{
this.questionHolder[numQuestions++] = Q;
}

public int giveQuiz()

{

Scanner scan = new Scanner (System.in);

String candidateAnswer;


System.out.println("start quiz?");
String y = scan.next();
if(y =="yes"){
for (int i = 0; i < numQuestions; i++)
{

candidateAnswer = scan.nextLine();
if (questionHolder[i].answerCorrect(candidateAnswer))
score++;
}

}
return getscore();
}
public int getscore()
{
return score;
}
public String toString()
{

return getscore() + "\n";
}

}

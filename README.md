#include <iostream>
#include <string>
#include <cstdlib>
using namespace std;
int main(){
  string i;
  string y;
  string o;
  string x;
  string b;
  int choice1 = 0;
  int choice2 = 0;
  srand(time(NULL));
  int outcome1 = std::rand() % 3;
   
  string ending1;
  string ending2;
  string ending3;

  std::cout << "Hello there adventurer! Please tell me your warrior's name.\n";
  std::cin >> i;
  //FIGURE OUT WHY YOU CAN'T PUT IN TWO WORDS 'EX. JUNKY JIMMY' SKIPS PICKING METHOD
  std::cout << "\nThank You! Next, select your adventurer's primary pronoun by choosing which number best suits your adventurer.\n";
  cout << "1. He/Him \n";
  cout << "2. She/Her \n"; 
  cout << "3. They/Them \n";
  cin >> choice1;

  while (choice1 >= 4) {
    cout << "Choice Invalid. Please re-enter your pronoun choice.\n";
    cout << "Select your adventurer's primary pronoun by choosing which number best suits your adventurer.\n";
    cout << "1. He/Him \n";
    cout << "2. She/Her \n"; 
    cout << "3. They/Them \n";
    cin >> choice1;
  }
  if(choice1 == 1){
    y = "Man";
    o = "He was";
    x = "Him";
    b = "Does He:";
  }
  else if(choice1 == 2){
    y = "Woman";
    o = "She was";
    x = "Her";
    b = "Does She:";
  }
  else {
    y = "Warrior";
    o = "They were";
    x = "Them";
    b = "Do they:";
  }
  cout << "There once was a " << y << " named " << i <<". ";
  cout << o << " great warrior and all the people in the village admired " << x <<". But " << i << " had a secrect.\n";
  cout << "With a heavy burdened heart, there was ultimately a choice to be made..." << b << ":\n";
  cout << "1) Tell the people but there is possibility they won't look at you the same.\n";
  cout << "2) Never tell them. But if they ever find out they'll turn their backs on you.\n";
  cout << "3) Or do you leave, never to return. Thus eliminating the threat of people finding out but loosing all that you held dear.\n";
  cin >> choice2;
  
  while(choice2 >= 4) {
    cout << "Invalid Entry, I understand the choices are hard but one must be made. Please decide, 1, 2, or 3.\n";
    cin >> choice2;
  }
  if(choice2 == 1) {
    cout << "You tell them...";
    switch(outcome1) {
      case 0 :
      cout << "and they understand. They commend you for your bravery and celebrate what you makes you special.\n";
      break;
      case 1 :
      cout << "and they understand. They commend you for your bravery and celebrate what you makes you special. Little do they know, that your secrect will ultimately be their demise.\n";
      break;
      case 2 :
      cout << "and are distraught. The village renounces you and shuns you. All you've done for them has been washed over with the news. In saddness you decide to leave this place you once called home.\n";
      break;
    }
  }
  else if(choice2 == 2) {
    cout << "You never tell them...";
    switch(outcome1) {
      case 0 :
      cout << "and they never find out. You spend your days thinking little on the growing problem. But at least nothing has changed. You're happy.\n";
      break;
      case 1 :
      cout << "and they never find out. You spend your days thinking on the growing problem. Worrisome days turn to sleepless nights. 'Will I lose control?' you continously ask yourself. But at least nothing has changed. You're happy. That is, until you do lose control.\n";
      break;
      case 2 :
      cout << "and they find out. The village confronts you, you look out to a see of people you once loved, now their eyes filled with hate. They chase you out the village and warm you to never come back. You are alone.\n";
      break;
      case 3 :
      cout << "and they find out. The village confronts you, you look out to a see of people you once loved, now their eyes filled with pity and saddness. They understand why you couldn't tell them but for the safety of the village you can't stay. They bid you farewel and shower you with love and gifts. Once you can control it, you know in your heart you can always come back.\n";
      break;
    }
  }
  else {
    cout << "You leave, and never return. You spend your days surviving in the lonely world. Sometimes at night you dream of those you loved. It's just enough of a reminder to continue to convince yourself 'this was the right choice'. But was it?\n";
  }
  cout << "\nThe End...\n\n";
}

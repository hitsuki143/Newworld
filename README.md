#include <iostream>
#include <string>
#include <cstdlib>
#include <ctime>

using namespace std;

// 🔁 Function to pause and wait for "E"
void pressToContinue() {
    string input;
    cout << "\n(Press 'E' then Enter to continue...)\n> ";
    getline(cin, input);
    while (input != "E" && input != "e") {
        cout << "Please press 'E' to continue.\n> ";
        getline(cin, input);
    }
}

int main() {
    string playerName;
    string choice;

    srand(time(0)); // Random number seed

    // 👤 Ask for player name
    cout << "Enter your name, visitor: ";
    getline(cin, playerName);

    cout << "Welcome " << playerName << " to our world!" << endl;
    cout << "Here you will meet and encounter all kinds of creatures!" << endl;
    cout << "Pay attention though—since we value your safety here, we advise you to choose someone to play with!" << endl;

    cout << "Do you want to play alone or with a companion? (type 'alone' or 'companion'): ";
    getline(cin, choice);

    if (choice == "alone") {
        cout << "You've chosen to be alone, huh? Interesting..." << endl;
        cout << "Very well then, " << playerName << ", you will be facing this world alone!" << endl;
    }
    else if (choice == "companion") {
        cout << "I knew you'd choose this, " << playerName << "!" << endl;
        cout << "You will be facing this world with your trusted companion!" << endl;
    }
    else {
        cout << "Since you haven't answered clearly, we'll just assume you're going alone..." << endl;
    }

    // 🌌 STORY STARTS HERE
    pressToContinue();
    cout << "\nYou woke up in an unusual place." << endl;
    pressToContinue();

    cout << "You're clearly outside, but you don't know where..." << endl;
    pressToContinue();

    cout << "You try to remember something... anything about the day before." << endl;
    pressToContinue();

    cout << playerName << ": \"Where the hell am I?!\"" << endl;
    pressToContinue();

    // 🧭 Continue adventure
    cout << "\nKeep going? (type 'yes' or 'no'): ";
    getline(cin, choice);

    if (choice == "yes") {
        cout << "It's a dark and cold night..." << endl;
        // More story can go here
    } else if (choice == "no") {
        cout << "Maybe next time, " << playerName << ". Goodbye!" << endl;
    } else {
        cout << "I'll take that as a no. Goodbye!" << endl;
    }

    return 0;
}

# CODSOFT
This repository contain 5 projects of Naveen vashist performing in CODSOFT as internship.

#include <iostream>
#include <random>
#include <vector>
#include <cstdlib>
#include <ctime>

using namespace std;
int main()
{
    srand(time(nullptr));
    int min = 0;
    int max = 100;
    int random_number = min + (rand() % (max - min + 1));
    int difference;
    cout << "start the game" << endl;
    cout << "time for user to choose a number [1,100]  : " << endl;
    while (true)
    {
        int Try;
        cin >> Try;

        difference = abs(random_number - Try);
        int close_range = 15;
        cout << "Randomly number is generated : " << endl;

        if (Try == random_number || difference == 0)
        {
            cout << "you won! guessed the exact number" << endl;
            break;
        }
        else if (difference <= close_range)
        {
            cout << "You are close! from The random number  " << endl;
            cout << "try again :";
        }
        else
        {
            cout << "you are far from  random number !" << endl;
            cout << "try again " << endl;
        }
    }
    return 0;
}

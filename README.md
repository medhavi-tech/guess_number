#include <iostream>
#include <cstdlib>
#include <ctime>

using namespace std;

int main() {
    // Seed the random number generator with current time
    srand(time(0));

    // Generate a random number between 1 and 100
    int secretNumber = rand() % 100 + 1;
    int guess;

    cout << "🎯 Welcome to the Number Guessing Game!\n";
    cout << "Guess a number between 1 and 100:\n";

    // Keep asking until the correct number is guessed
    while (true) {
        cout << "Enter your guess: ";
        cin >> guess;

        if (guess < secretNumber) {
            cout << "Too low! Try again.\n";
        } else if (guess > secretNumber) {
            cout << "Too high! Try again.\n";
        } else {
            cout << "🎉 Congratulations! You guessed the correct number: " << secretNumber << endl;
            break;
        }
    }

    return 0;
}



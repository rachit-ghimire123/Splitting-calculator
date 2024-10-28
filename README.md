
#include <iostream>
#include <iomanip> // Include for std::setprecision
using namespace std;

// Function to calculate the amount each person should pay
double splitBill(double totalAmount, int numberOfPeople) {
    return totalAmount / numberOfPeople;
}

int main() {
    double totalAmount;
    int numberOfPeople;

    // Input: Total bill amount and number of people
    cout << "Enter the total bill amount: $";
    cin >> totalAmount;
    cout << "Enter the number of people: ";
    cin >> numberOfPeople;

    // Check if the number of people is valid
    if (numberOfPeople <= 0) {
        cout << "The number of people must be greater than 0" << endl;
    }

    // Calculate and display the amount each person should pay
    double amountPerPerson = splitBill(totalAmount, numberOfPeople);
  
    // Set precision to 2 decimal places
    cout << fixed << setprecision(2);
    cout << "Each person should pay: $" << amountPerPerson << endl;

    return 0;
}

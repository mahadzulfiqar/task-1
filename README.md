# task-1
#include <iostream>
using namespace std;

int main() {
    double temperature;
    char unit;

    // Prompt user to enter temperature and the unit
    cout << "Enter the temperature value: ";
    cin >> temperature;
    cout << "Enter the unit of the temperature (C for Celsius, F for Fahrenheit, K for Kelvin): ";
    cin >> unit;

    double celsius, fahrenheit, kelvin;

    // Convert based on the input unit
    if (unit == 'C' || unit == 'c') {
        celsius = temperature;
        fahrenheit = (celsius * 9/5) + 32;
        kelvin = celsius + 273.15;
    } else if (unit == 'F' || unit == 'f') {
        fahrenheit = temperature;
        celsius = (fahrenheit - 32) * 5/9;
        kelvin = celsius + 273.15;
    } else if (unit == 'K' || unit == 'k') {
        kelvin = temperature;
        celsius = kelvin - 273.15;
        fahrenheit = (celsius * 9/5) + 32;
    } else {
        cout << "Invalid unit entered!" << endl;
        return 1; // Exit the program with an error code
    }

    // Display the converted values
    cout << "Temperature in Celsius: " << celsius << " °C" << endl;
    cout << "Temperature in Fahrenheit: " << fahrenheit << " °F" << endl;
    cout << "Temperature in Kelvin: " << kelvin << " K" << endl;

    return 0;
}

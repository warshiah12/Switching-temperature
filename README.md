# Switching-temperature
temperature conversion using switch
#include<iostream>
using namespace std;
int main()
{
	char choice;   //declaring variable 'choice' with datatype char
	double fahren;  //declaring variable 'fahren' with datatype double
	double cels;    //declaring variable 'cels' with datatype double

	cout << "Enter the type of conversion. \n'F' for fahrenheit to celsius conversion and 'C' for celsius to fahrenheit conversion :" << " ";
	cin >> choice;

	switch (choice)  //the input entered by the user will be evaluated
	{
	case 'F':     //if he enters 'f' or 'F' then the following message will be displayed
	case'f':
		cout << "You chose Fahrenheit to celsius conversion. \nCelsius= (fahrenheit-32)*5/9 " << endl;

		cout << "\nEnter the temperature in Fahrenheit: " << endl;  //the user will enter the temperature to be converted
		cin >> fahren;
		cels = (fahren - 32) * 5 / 9;  //formula to convert temperature from fahrenheit to celsius

		cout << "\nCelsius= " << cels << endl;
		break;
	case 'C':   //if he enters 'c'or 'C'then the following message will be displayed
	case 'c':
		cout << "\nYou chose Celsius to Fahrenheit conversion \nFahrenheit= (Celsius*9/5)+32 " << endl;
		cout << "\nEnter the temperature in Celsius: " << endl;   //the user will enter the temperature to be converted
		cin >> cels;
		fahren = (cels * 9 / 5) + 32;   //formula to convert temperature from celsius to fahrenheit
		cout << "\nFahrenheit= " << fahren << endl;
		break;
	default:      //if he enters any other alphabet besides c and f then the default case will be executed
		cout << "\nInvalid conversion...." << endl;
		break;
	}
	return 0;
}

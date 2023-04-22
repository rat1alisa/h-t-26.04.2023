# h-t-26.04.2023

//TASK 1.1
#include <iostream>
#include <cmath>
using namespace std;

class Fraction
{
public:
    int a, b;
    int c, d; 
};
//----------------------------------
Fraction operator * (const Fraction& a1, const Fraction& d2) 
{
    return Fraction{ a1.a * d2.d };
};
Fraction operator * (Fraction& c1, Fraction& b1)
{
    return Fraction{ c1.c * b1.b };
};
//----------------------------------
int main()
{
    cout << "\t\t Fraction program 2.0" << endl;
    Fraction f1;
    Fraction f2;
    cout << "Enter values for the first fraction: " << endl;
    cout << "\tNumerator -> ";
    cin >> f1.a;
    cout << "\tDenominator -> ";
    cin >> f1.b;

    Fraction f12;
    Fraction f22;
    cout << "Enter values for the second fraction:" << endl;
    cout << "\tNumerator -> ";
    cin >> f12.c;
    cout << "\tDenominator -> ";
    cin >> f22.d;
    //-----------
    int a;
	do {
		cout << "\n1. Addition.";
		cout << "\n2. Substraction.";
		cout << "\n3. Multiplication.";
		cout << "\n4. Division." << endl;
		cout << "\nSelect the required operation - ";
		cin >> a;
		switch (a)
		{
		case 1: (a = 1);
			cout << (f1.a * f22.d) + (f1.b * f12.c) << '/' << f1.b * f22.d << endl;
			break;
		case 2: (a = 2);
			cout << (f1.a * f22.d) - (f1.b * f12.c) << '/' << f1.b * f22.d << endl;
			break;
		case 3: (a = 3);
			cout << (f1.a * f22.d) / (f1.b * f12.c) << '/' << f1.b * f22.d << endl;
			break;
		case 4: (a = 4);
			cout << (f1.a * f22.d) * (f1.b * f12.c) << '/' << f1.b * f22.d << endl;
			break;
		case 5: (a = 5);
			break;
		}
	}
	while (a != 5);
	    cout << "Programm stopped.\n";
	system ("color 5");
	return 0;
}

//TASK 1.2

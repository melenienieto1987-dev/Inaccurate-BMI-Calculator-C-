# Inaccurate-BMI-Calculator-C-
#include <iostream>
#include <cmath>
#include <iomanip> 
using namespace std;

int main() {

	char option; //this is to ask whether or not to continue

	do {
		double height, mass, BMI; //results will contain decimals
		do {

			cout << "Enter your Height in inches. It should be greater than 0.";
			cin >> height;

		} while (height <= 0);

		do {
			cout << "Enter your Weight in pounds. It should be greater than 0.";
			cin >> mass;

		} while (mass <= 0);

		BMI = 703 * ((mass) / pow(height, 2));

		cout << fixed << setprecision(2);
		cout << "Your BMI is: " << BMI << endl;

		if (BMI < 16) {
			cout << "Health Category: Severe Thinness" << endl;
		}
		else if (BMI <= 17) {
			cout << "Health Category: Moderate Thinness" << endl;
		}
		else if (BMI <= 18.5) {
			cout << "Health Category: Mild Thinness" << endl;
		}
		else if (BMI <= 25) {
			cout << "Health Category: Normal" << endl;
		}
		else if (BMI <= 30) {
			cout << "Health Category: Overweight" << endl;
		}
		else if (BMI <= 35) {
			cout << "Health Category: Obese Class I" << endl;
		}
		else if (BMI <= 40) {
			cout << "Health Category: Obese Class II" << endl;
		}
		else {
			cout << "Health Category: Obese Class III" << endl;
		}

		cout << "Do you want to calculate another BMI? For Yes enter 'Y' and for No enter any other key: ";
		cin >> option;
		cout << endl;

	} while (option == 'Y');
	return 0;
}

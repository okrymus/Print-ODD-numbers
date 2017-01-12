// The program will output OOD numbers in a user inputed a range.
// Output OOD numbers in a user inputed a range
// Programmer: Panupong Leenawarat
// Last modify: 10/31/15

#include <iostream>
using namespace std;

int main()
{
	double startPoint, endPoint;
	//Title
	cout
		<< endl
		<< "\t  This program will output OOD numbers in a user inputed a range.  \n"
		<< "\t                      by Lee. Panupong			                   " 
		<< endl;

	while (true)
	{
		cout << "\nEnter the starting point of the range(double) : ";
		cin >> startPoint;	 cin.ignore(80, '\n');
		cout << "Enter the ending point of the range (double): ";
		cin >> endPoint;	 cin.ignore(80, '\n');
		
		while (endPoint <= startPoint)
		{ 
			cout << "Your ending number must be greater than your starting number.\n"
				<< "Please try a new ending number :";
			cin >> endPoint;    cin.ignore(80, '\n');
		}

		startPoint = (int)ceil(startPoint);
		for (startPoint = ((int)startPoint % 2 == 0 ? startPoint + 1 : startPoint); startPoint <= endPoint; startPoint += 2)
			cout << startPoint << " ";
		cout << endl;
	}
}
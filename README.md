#include <iostream>
#include <fstream>
#include <string>

using namespace std;

int main()
{
	int sumofAge = 0;
	double sumofScore = 0;
	int maleNo = 0;
	int femaleNo = 0;
	struct student
	{
		string name;
		string id;
		int age;
		char gender = ' ';
		double score = -1;
		char grade;
	};

	student a[2];

	for(int i = 0; i <= 1; i++)
	{
		cout << "Enter Name: ";
		cin >> a[i].name;
		cout << "Enter ID number: ";
		cin >> a[i].id;
		cout << "Enter Age: ";
		cin >> a[i].age;
		
		while(true)
		{
			cout << "Enter Gender: ";
			cin >> a[i].gender;
			if(a[i].gender == 'M' || a[i].gender== 'm' ||a[i].gender == 'f' || a[i].gender == 'F')
				break;
		}
		
		while(true)
		{
			cout << "Enter Score: ";
			cin >> a[i].score;
			if(a[i].score >= 0 && a[i].score <= 100)
				break;
		}

		if(a[i].score >= 80)
   a[i].grade= 'A'
	
	else if(a[i].score >= 70 && a[i].score<80)
			a[i].grade = 'B';
		else if(a[i].score >= 60 && a[i].score<70)
			[hsjsi].grade = 'C';
		else if(students[i].score >= 50)
			stui].grade = 'D';
		else if(students[i].score >= 40)
			students[i].grade = 'E';
		else
			students[i].grade = 'F';

		// computations
		totalAge += students[i].age;
		totalScore += students[i].score;
		if(students[i].gender == 'M')
			maleCount += 1;
		else if(students[i].gender == 'F')
			femaleCount += 1;

		cout << endl << endl;
	

	// write records to file
	fstream file;
	file.open("output.txt", ios::out);
	for(int i = 0; i <= 1; i++)
	{
		file << i+1 << ".  ";
		file << students[i].idNumber << "  ";
		file << as[i].name << "  ";
		file << students[i].age << "  ";
		file << students[i].gender << "  ";
		file << students[i].score << "  ";
		file << students[i].grade << endl;

		cout << "Record " << i+1 << " was successfully written to file." << endl;
	}
	file << endl << "Average age: " << totalAge / 5 << endl;
	file << "Average score: " << totalScore / 5 << endl;
	file << "Male count: " << maleCount << endl;
	file << "Female count: " << femaleCount << endl;
	return 0;
}

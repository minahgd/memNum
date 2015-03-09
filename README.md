// memNum.cpp : Defines the entry point for the console application.
//

#include "stdafx.h"
#include <iostream>
#include <fstream>
#include <string>

using namespace std;

void numWords(char[], char[][4]);
void printWords(char[][4]);
int _tmain(int argc, _TCHAR* argv[])
{
	char phoneNumArr[7];
	char phoneWord[7][4];
	string phoneNum;
	

	cout << "Enter a phone number: (e.g. 223-4567 NO 1'S OR 0'S) ";
	cin >> phoneNum;

	for (int i = 0; i < 7; i++)
	{
		if (i >= 3)
		{
			phoneNumArr[i] = phoneNum.at(i + 1);
		}
		else
			phoneNumArr[i] = phoneNum.at(i);
	}	

	numWords(phoneNumArr, phoneWord);
	printWords(phoneWord);
	
	system("pause > NULL");
	return 0;
}

void numWords(char arrNum[], char arrWord[][4])
{
	for (int i = 0; i < 7; i++)
	{
		if (arrNum[i] == '2')
		{
			arrWord[i][0] = 'A';
			arrWord[i][1] = 'B';
			arrWord[i][2] = 'C';
		}

		if (arrNum[i] == '3')
		{
			arrWord[i][0] = 'D';
			arrWord[i][1] = 'E';
			arrWord[i][2] = 'F';
		}

		if (arrNum[i] == '4')
		{
			arrWord[i][0] = 'G';
			arrWord[i][1] = 'H';
			arrWord[i][2] = 'I';
		}

		if (arrNum[i] == '5')
		{
			arrWord[i][0] = 'J';
			arrWord[i][1] = 'K';
			arrWord[i][2] = 'L';
		}

		if (arrNum[i] == '6')
		{
			arrWord[i][0] = 'M';
			arrWord[i][1] = 'N';
			arrWord[i][2] = 'O';
		}

		if (arrNum[i] == '7')
		{
			arrWord[i][0] = 'P';
			arrWord[i][1] = 'Q';
			arrWord[i][2] = 'R';
			arrWord[i][3] = 'S';
		}

		if (arrNum[i] == '8')
		{
			arrWord[i][0] = 'T';
			arrWord[i][1] = 'U';
			arrWord[i][2] = 'V';
		}

		if (arrNum[i] == '9')
		{
			arrWord[i][0] = 'W';
			arrWord[i][1] = 'X';
			arrWord[i][2] = 'Y';
			arrWord[i][3] = 'Z';
		}	
	}
}

void printWords(char arrWord[][4])
{
	for (int i = 0; i < 7; i++)
	{
		cout << arrWord[i][0];
	}

	cout << endl;

	for (int i = 0; i < 7; i++)
	{
		cout << arrWord[i][1];
	}

	cout << endl;

	for (int i = 0; i < 7; i++)
	{
		cout << arrWord[i][2];
	}
}



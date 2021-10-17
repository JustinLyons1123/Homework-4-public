# Homework-4-public
homework 4 public

// C++ program to print all
// permutations with duplicates allowed
#include <iostream>
using namespace std;


// Function to print permutations of string
// This function takes three parameters:
// 1. String
// 2. Starting index of the string
// 3. Ending index of the string.
void permute(string a, int l, int r)
{
	// Base case
	if (r == 1)
	{
		cout << a << endl;
	}
	else
	{
		// Permutations made
		for (int i = l; i <= r; i++)
		{

			// Swapping done
			swap(a[l], a[i]);

			// Recursion called
			permute(a, l + 1, r);

			//backtrack
			swap(a[l], a[i]);
		}
	}
}

// Driver Code
int main()
{
	int k;
	string str;

	cout << "Please enter the number of items to be permuted:";
	cin >> k;
	cout << "Please enter the items to be permuted:";
	cin >> str;
	
	permute(str, 0, k - 1);
	return 0;
}

// This is code is contributed by rathbhupendra

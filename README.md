# Homework-4-public
homework 4 public

#include <iostream>
using namespace std;

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


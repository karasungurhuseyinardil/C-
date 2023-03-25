template <class type> 
 ref – type func -  name(parameter list)
 {
	body of the function
 }	

#include <iostream>
#include <string>
using namespace std;

template<typename T>

inline T const& Max(T const& a, T const& b)
{
	return a < b ? b : a;
}

int main()
{
	string s1 = "Hello";
	string s2 = "World";
cout << "Max(s1,s2) :  " << Max(s1, s2) <<endl;

	int i = 34;
	int j = 41;
	cout << "Max(i,j) : " << Max(i, j) << endl;

	double x = 17.8;
	double y = 25.4;
	cout << "Max(x,y) : " << Max(x, y) << endl;
	system("pause");
	return 0;
}


#include <iostream>
using namespace std;

int main() 
 {
	 //Declare a pointer to an integer
	int* ptr;

	  //Dynamically allocate memory for an integer using new
  ptr = new int;

// Check if memory allocation was successful
	if (ptr == NULL) 
	{
		cout << "Memory allocation failed" << endl;
		return 1;
	}
// Store a value in the dynamically allocated memory
	*ptr = 42;
	
// Print the value of the dynamically allocated memory
cout << "The value of the dynamically allocated memory is: " << *ptr << endl;
// Free the dynamically allocated memory using delete 
	delete ptr;
	system("pause");
	return 0;
}


#include <iostream>  
using namespace std;
int main()
{
	 //Pointer initialization to null  
	int* m = NULL;

//Request memory for the variable using new operator  
	m = new(nothrow) int;
	if (!m)
		cout << "allocation of memory failed\n";
	else
	{	//Store value at allocated address  
		*m = 39;
		cout << "Value of m: " << *m << endl;
	}
// Request block of memory  using new operator  
	float *f = new float(40.25);
	cout << "Value of f: " << *f << endl;

	 //Request block of memory of size   
	int size = 5;
	int *arr = new(nothrow) int[size];
	if (!arr)
		cout << "allocation of memory failed\n";
	else
	{
		for (int i = 0; i< size; i++)
			arr[i] = i + 1;

		cout << endl << endl;

cout << "Value store in block of memory:\n ";
		for (int i = 0; i<size; i++)
			cout << arr[i] << " ";

		cout << endl << endl;

		cout << "Value store in block of memory as reverse list: \n";

		for (int j = size - 1; j >= 0; j--)
			cout << arr[j] << " ";

	cout << endl << endl;
}

	 //freed the allocated memory  
	delete m;
	delete f;
	 //freed the block of allocated memory  
	delete[] arr;
	system("pause");
	return 0;
}



Fibonacci Sequence
The Fibonacci Sequence is the series of numbers :
0, 1, 1, 2, 3, 5, 8, 13, 21, 34, ...

The next number is found by adding up the two numbers before it.
•	The 2 is found by adding the two numbers before it(1 + 1)
•	The 3 is found by adding the two numbers before it(1 + 2),
•	And the 5 is (2 + 3),
•	and so on!

	try  to solve this problem with using recursive function 


#include <iostream>
using namespace std;

int fibonacci(int n) 
{
//	if (n <= 1)  // base cases
//		return n;

	if ((n== 1) || (n == 0)) 
	{
		return n;
	}
	else
	{            // recursive case
	return fibonacci(n - 1) + fibonacci(n - 2);
	}
}

int main() {
	int n;
	cout << "Enter a positive integer: ";
	cin >> n;
	cout << "Fibonacci sequence up to " << n << " terms:" << endl;

	for (int i = 0; i < n; i++) 
	{
		cout << fibonacci(i) << " ";
	}
	cout << endl;
	system("pause");
	return 0;
}

CAN YOU WRITE A RECURSIVE FUNCTION 
THAT PRINTS THE ELEMENTS OF A GIVEN ARRAY FROM THE GIVEN INDEX (as a start point) TO THE SCREEN ?

 FUNCTION TAKES 3 PARAMETERS AS
 1st parameter ???                  
 2nd parameter ???				   
 3rd parameter ???

#include <iostream>  
using namespace std;

void print_array(int arr[], int size, int i)
{
	if (i == size) 
	{
		cout << endl;
		return;
	}

	cout << arr[i] << " ";
	i++;

	print_array(arr, size, i);
}

int main()
{
	int arr[] = { 3, 5, 6, 8, 1 };
	int n = sizeof(arr) / sizeof(arr[0]);

	print_array(arr, n, 0);
	print_array(arr, n, 1);
	print_array(arr, n, 2);
	system("pause");
	return 0;
}


#include <iostream>
using namespace std;

int main() {
	int numbers[5] = { 10, 20, 30, 40, 50 };
	int *p;

	p = numbers;

	cout << "Array elements using pointer index ++:" << endl;
	for (int i = 0; i < 5; i++)
	{
		cout << "*(p + " << i << ") = " << *(p + i) << endl;
	}

	p = numbers;
	cout << "\nArray elements using pointer index ++ after increment:" << endl;
	for (int i = 0; i < 5; i++) 
	{
		cout << "*(p++) = " << *(p++) << endl;
	}
	

	cout << *(p-1) << endl;
    cout << *(p-2) <<endl;
    cout << *(p-3) <<endl;

	system("pause");
	return 0;
}

// C++ Implementation of the Quick Sort Algorithm.
#include <iostream>
using namespace std;

int partition(int arr[], int start, int end)
{

	int pivot = arr[start];

	int count = 0;
	for (int i = start + 1; i <= end; i++)
	{
		if (arr[i] <= pivot)
			count++;
	}

	// Giving pivot element its correct position
	int pivotIndex = start + count;  
	swap(arr[pivotIndex], arr[start]); 

	// Sorting left and right parts of the pivot element
	int i = start, j = end;

	while (i < pivotIndex && j > pivotIndex)
	{

		while (arr[i] <= pivot) 
		{
			i++;
		}

		while (arr[j] > pivot) 
		{
			j--;
		}

		if (i < pivotIndex && j > pivotIndex) 
		{
			swap(arr[i++], arr[j--]);
		}
	}

	return pivotIndex;
}

void quickSort(int arr[], int start, int end)
{

	// base case
	if (start >= end)
		return;

	// partitioning the array
	int p = partition(arr, start, end);

	// Sorting the left part
	quickSort(arr, start, p - 1);  

	// Sorting the right part
	quickSort(arr, p + 1, end);
}

int main()
{
int arr[] = { 9, 3, 4, 2, 1, 7, 5, 8, 3, 4, 7};
int n = 11;

	quickSort(arr, 0, n - 1);

	for (int i = 0; i < n; i++) {
		cout << arr[i] << " ";
	}
	cout << endl << endl;
	system("pause");
	return 0;
}


class CLASS-NAME
{
	ACCESS - SPECIFIER:
	DATA - VARIABLE;

	MEMBER - FUNCTION
	{
		BODY
	}
};




#include <iostream>
using namespace std;

class Rectangle{
private:
	int l, w;
public:
	void input(int len, int wid)
	{
		l = len;
		w = wid;
	}

	int area()
	{
		return l * w;
	}
};

int main()
{
	Rectangle r1, r2;

	r1.input(10, 7);
	r2.input(9, 4);
	cout << "Area of r1: " << r1.area() << endl;
	cout << "Area of r2: " << r2.area() << endl;

	system("pause");
	return 0;
}


#include <iostream>
#include <string>
using namespace std;

class Student {
private:
	string name;
	int age;
	string major;

public:
	Student(string nm, int ag, string mj) 
	{
		name = nm;
		age = ag;
		major = mj;
	}

	void setName(string nm)
	{
		name = nm;
	}

	void setAge(int ag)
	{
		age = ag;
	}

	void setMajor(string mj)
	{
		major = mj;
	}

	string getName()
	{
		return name;
	}

	int getAge()
	{
		return age;
	}

	string getMajor() 
	{
		return major;
	}

	void printInfo() 
	{
		cout << "Name: " << name << endl;
		cout << "Age: " << age << endl;
		cout << "Major: " << major << endl;
	}
};



int main() 
{
	Student s("John ", 20, "Computer Science");

	s.printInfo();

	s.setAge(21);
	s.setMajor("Information Technology");

	cout << endl;

	s.printInfo();
	system("pause");
	return 0;
}




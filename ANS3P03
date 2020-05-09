
#include <iostream>
#include <string.h>
using namespace std;

#define MAX 1000
void heapify(char arr[], int n, int i)
{
	int largest = i;
	int l = 2 * i + 1;
	int r = 2 * i + 2;


	if (l < n && arr[l] > arr[largest])
		largest = l;


	if (r < n && arr[r] > arr[largest])
		largest = r;

    if (largest != i) {
		swap(arr[i], arr[largest]);
        heapify(arr, n, largest);
	}
}

void build(char arr[], int n)
{

	int startIdx = (n / 2) - 1;

	for (int i = startIdx; i >= 0; i--) {
		heapify(arr, n, i);
	}
}
void displayHeap(char arr[], int n)
{
	cout << "Array representation of Heap is:\n";

	for (int i = 0; i < n; ++i)
		cout << arr[i] << " ";
	cout << "\n";
}
void heapify1(char arr[], int n, int i)
{

	int parent = (i - 1) / 2;

	if (arr[parent] > 0) {

		if (arr[i] > arr[parent]) {
			swap(arr[i], arr[parent]);


			heapify1(arr, n, parent);
		}
	}
}
void insert(char arr[], int& n, char Key)
{

	n = n + 1;

	arr[n - 1] = Key;
     heapify1(arr, n, n - 1);
}

void displayArray1(char arr[], int n)
{ cout<<"final max heap is\n";
	for (int i = 0; i < n; ++i)
		cout << arr[i] << " ";

	cout << "\n";
}
int main()
{

string s;
    cout << "Enter a first name: ";
    getline(cin, s);

    cout << "You entered: " << s << endl;



    int y = s.length();


    char arr[y + 1];

        strcpy(arr, s.c_str());

    for (int i = 0; i < y; i++)
        cout << arr[i];

	 int n = sizeof(arr) / sizeof(arr[0]);

	build(arr, n);

	displayHeap(arr, n);
///
string s2;
    cout << "Enter a second name: ";
    getline(cin, s2);

    cout << "You entered name is: " << s2 << endl;



    int w = s2.length();


    char arr1[w+ 1];

    strcpy(arr1, s2.c_str());




for (int i = 0; i < w; ++i){


	char key = arr1[i];

	insert (arr, n, key);
}
	displayArray1(arr, n);

	return 0;
}

#include <iostream>
using namespace std;

int linear_search(int array[], int n, int target) {
    for (int i = 0; i < n; i++) {
        if (array[i] == target)
            return i; 
    }
    return -1; 
}

int main() {
    int numbers[] = {10, 25, 30, 45, 50};
    int target_value = 30;
    int length = sizeof(numbers) / sizeof(numbers[0]);

    int index = linear_search(numbers, length, target_value);

    if (index != -1)
        cout << "Target found at index " << index << endl;
    else
        cout << "Target not found in the array." << endl;

    return 0;
}


//Expected Output:
Target found at index 2

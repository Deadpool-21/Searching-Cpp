#include <iostream>
using namespace std;

int sequential_search(int array[], int n, int target) {
    int index = 0;
    while (index < n) {
        if (array[index] == target)
            return index; 
        index++;
    }
    return -1; 
}

int main() {
    int numbers[] = {5, 15, 25, 35, 45};
    int target_value = 25;
    int length = sizeof(numbers) / sizeof(numbers[0]);

    int result = sequential_search(numbers, length, target_value);

    if (result != -1)
        cout << "Target found at index " << result << endl;
    else
        cout << "Target not found in the array." << endl;

    return 0;
}


//Expected Output:
Target found at index 2

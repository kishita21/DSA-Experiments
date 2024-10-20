#include <stdio.h>
// Function to implement binary search
int binarySearch(int arr[], int n, int target) {
int low = 0, high = n - 1;
while (low <= high) {
int mid = low + (high - low) / 2;
// Check if the middle element is the target
if (arr[mid] == target) {
return mid; // Target found at index 'mid'
}
// If target is greater than mid, search in the right half
if (arr[mid] < target) {
low = mid + 1;
}
// If target is smaller than mid, search in the left half
else {
high = mid - 1;
}
}
return -1; // Target not found
}
// Driver code for real-life application (student roll number search)
int main() {
int n, target, result;
printf("Enter the number of students: ");
scanf("%d", &n);
int rollNumbers[n]; // Array to store roll numbers of students
(sorted)
printf("Enter the sorted roll numbers of students:\n");
for (int i = 0; i < n; i++) {
scanf("%d", &rollNumbers[i]);
}
// Input the roll number to search
printf("Enter the roll number to search: ");
scanf("%d", &target);
// Perform binary search
result = binarySearch(rollNumbers, n, target);
// Display the result
if (result != -1) {
printf("Student with roll number %d found at position %d.\n",
target, result + 1);
} else {
printf("Student with roll number %d not found.\n", target);
}
return 0;
}

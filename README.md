
#include <iostream.h>
#include <conio.h>

int isPalindrome(int num) {
    int originalNum = num;
    int reversedNum = 0, remainder;

    while (num != 0) {
        remainder = num % 10;
        reversedNum = reversedNum * 10 + remainder;
        num = num / 10;
    }

    if (originalNum == reversedNum)
        return 1;   
    else
        return 0;   
}

void main() {
    int num;
    clrscr();

    cout << "Enter a number: ";
    cin >> num;

    if (isPalindrome(num))
        cout << "\nThe number is a palindrome.";
    else
        cout << "\nThe number is not a palindrome.";

    getch();
}

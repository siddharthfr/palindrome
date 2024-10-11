palindrome
palindrome codes

#include <stdio.h>
int main() {
    char str[100];
    int i, j, len;
    int isPalindrome = 1;
    
    printf("Enter a string: ");
    scanf("%s", str);
    
    len = length(str);
    
    for (i = 0, j = len - 1; i < len / 2; i++, j--) {
        if (str[i] != str[j]) {
            isPalindrome = 0;
            break;
        }
    }
    
    if (isPalindrome) {
        printf("%s is a palindrome", str);
    } else {
        printf("%s is not a palindrome", str);
    }
    
    return 0;
}
int length(char x[]){
	int i=0;
	while(x[i]!='\0'){
		i++;
	}
	return i;
}

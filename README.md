q1.
#include <stdio.h>
void reverseString(char str[]) {
     int len = 0;
    while (str[len] != '\0') {
        len++;
    }
     for (int i = 0; i < len / 2; i++) {
        char temp = str[i];
        str[i] = str[len - i - 1];
        str[len - i - 1] = temp;
    }
}

int main() {
    char str[100]; // Assuming the maximum length of the string is 100
  printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);
  
    if (str[strlen(str) - 1] == '\n') {
        str[strlen(str) - 1] = '\0';
    }
 
    reverseString(str);
    
   
    printf("Reversed string: %s\n", str);
    
    return 0;
}

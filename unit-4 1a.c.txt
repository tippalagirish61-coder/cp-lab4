//program to write data into a file
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>
int main() {
    FILE* fp;
    fp = fopen("data.txt", "r");   // Opens file for writing (creates/overwrites)
    if (fp == NULL) {
        printf("File cannot be opened!\n");
        return 1;
    }
    fprintf(fp, "Welcome to File Handling in C\n");
    fprintf(fp, "This text is written to the file.\n");
    fclose(fp);
    printf("Data written successfully.\n");
    return 0;
}

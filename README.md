#include <stdio.h>
#include <string.h>
#include <ctype.h>
#define char_count 256
int main()
{
    char str[100];
    int v=0,c=0,s=0,d=0,i;
    printf("enter the string");
    fgets(str, sizeof(str), stdin);
    for(i=0;str[i] != '\0';i++){
        char ch= tolower(str[i]);
        if(ch>='a' && ch<= 'z'){
            if(ch=='a'|| ch=='e'|| ch=='i' || ch=='o' || ch=='u')
            v++;
            else
            c++;
        }
        else if (ch== ' '){
            s++;
        }else if(isdigit(ch)){
            d++;
        }
    }
    printf("vowels %d\n",v);
    printf("consonents %d\n",c);
    printf("spaces %d\n",s);
    printf("digits %d\n",d);
    return 0;
}

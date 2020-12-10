#include #include

using namespace std;

int main() { char str[] = "Something"; char *start, *end, *p; int len; int t;

cout << "The strart string :  " << str << "\n";

len = strlen(str);

start = str;
end = &str[len - 1];
 p = str;
while(*p){ if(isupper(*p)) *p = tolower(*p); else if(islower(*p)) *p = toupper(*p); p++; }

while(start < end){
    t = *start;
    *start = *end;
    *end = t;

    start++;
    end--;
}

cout << "The reversed string:  " << str;

return 0;
}



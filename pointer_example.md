## pass by reference (&)

```c++
#include<iostream>
int add_some(int &);

int main(){
  int a = 10;
  printf("%d\n",a);
  add_some(a);
}

int add_some(int & b){
  b++;
  printf("b=%d\n",b);
  
}
```

#### Output
```
b = 11
a = 11
```

## read only reference
```c++
#include<iostream>
int add_some(int &);

int main(){
  int a = 10;
  printf("%d\n",a);
  add_some(a);
}

int add_some(int & b){
  b++;
  printf("b=%d\n",b);
  
}
```
### output
```
  error: (b++) not allowed in read only reference
```


## passing array 
```c++
#include<iostream>
int add_some(int [], int);
void display(int [],int);

int main(){
  int limit = 4;
  int a[] = {10,20,30,40};
  add_some(a, limit);
  printf("a[]\n");
  display(a, limit);
}

int add_some(int b[], int limit){
  printf("b[]\n");
  display(b, limit);
}


void display(int array[], int limit){
    for (int i=0; i< limit; i++)
    printf("\telement %d = %d\n",i,array[i]);
}
```

### Output
```
b[]
	element 0 = 10
	element 1 = 20
	element 2 = 30
	element 3 = 40
a[]
	element 0 = 10
	element 1 = 20
	element 2 = 30
	element 3 = 40
```  

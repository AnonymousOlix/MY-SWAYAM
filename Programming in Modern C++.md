# Programming in Modern C++

# Week 5 

# Programming Assignment 1

```bash
class Employee : private Contact {
    private:
        int emp_id;
        string emp_name;
    public:
        Employee(int emp_id_, string emp_name_, int phone_number_, string email_) 
          : emp_id(emp_id_), emp_name( emp_name_), Contact(phone_number_ , email_){}    // LINE-1
        using Contact::displayContact;   // LINE-2
        void display(){
            cout << "ID: " << emp_id << endl;
            cout << "Name: " << emp_name << endl;
        }
};
```

# Programming Assignment 2

```bash
#include <iostream>
using namespace std;
 
class Appliance {
protected:
    int power;
 
public:
    Appliance(int p) : power(p) {}
 
    friend ostream& operator<<(ostream& os, const Appliance& a);
};
 
class WashingMachine : public Appliance{  // LINE-1
protected:
    int drum_size;
 
public:
    WashingMachine(int p, int ds) :  drum_size(ds), Appliance(p) {}  // LINE-2
 
    friend ostream& operator<<(ostream& os, const WashingMachine& wm);
};
 
class Refrigerator : public Appliance {  // LINE-3
protected:
    int capacity;
 
public:
    Refrigerator(int p, int c) :  Appliance(p), capacity(c){}  // LINE-4
 
    friend ostream& operator<<(ostream& os, const Refrigerator& r);
};
```

# Programming Assignment 3

```bash
X::X(int _x) : x(_x) {}    //LINE-1
 
Y::Y(int _x, int _y) :  X(_x), y(_y) {}    //LINE-2
 
Z::Z(int _x, int _y, int _z) : Y(_x,_y), z(_z) {}    //LINE-3
 
int X::getSum(){  return x; }    //LINE-4 
 
int Y::getSum(){ return X::getSum() + y; }    //LINE-5
 
int Z::getSum(){ return Y::getSum() + z; }    //LINE-6
```


### Congratulations 🎉 You Completed Assignment !

##### *You Have Successfully Demonstrated Your Skills And Determination.*

#### *Well done!*

# [MY SWAYAM](https://www.youtube.com/@MySwayam)

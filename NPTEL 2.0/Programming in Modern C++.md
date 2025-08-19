# Programming in Modern C++

# Week 5 

# Programming Assignment 1

```bash
class Student : public Contact {  // Changed from private to public inheritance
private:
    int roll_no;
    string name;
public:
    // LINE-1: Initialization list
    Student(int roll_no_, string name_, int phone_no_) 
        : Contact(phone_no_), roll_no(roll_no_), name(name_) {}

    void print() {
        cout << "roll: " << roll_no << endl;
        cout << "name: " << name << endl;
    }
};
```

# Programming Assignment 2

```bash
class Car : public Vehicle {    //LINE-1
    protected: 
        int no_of_passengers;
    public:
        Car(int nw, int np) : Vehicle(nw), no_of_passengers(np) {} //LINE-2
        friend ostream& operator<<(ostream& os, const Car& d); 
};

class Truck : public Vehicle {    //LINE-3
    protected: 
        int load_capacity;
    public:
        Truck(int nw, int lc) : Vehicle(nw), load_capacity(lc) {} //LINE-4
        friend ostream& operator<<(ostream& os, const Truck& d); 
};
```

# Programming Assignment 3

```bash
// LINE-1
A::A(int _a): a(_a) {}

// LINE-2
B::B(int a, int b): A(a), b(b) {}

// LINE-3
C::C(int a, int b, int _c): B(a, b), c(_c) {}

// LINE-4
int A::sum() { return a; }

// LINE-5
int B::sum() { return A::sum() + b; }

// LINE-6
int C::sum() { return B::sum() + c; }
```

### Congratulations 🎉 You Completed Assignment !

##### *You Have Successfully Demonstrated Your Skills And Determination.*

#### *Well done!*

# [MY SWAYAM](https://www.youtube.com/@MySwayam)

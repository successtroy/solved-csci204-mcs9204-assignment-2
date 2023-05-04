Download Link: https://assignmentchef.com/product/solved-csci204-mcs9204-assignment-2
<br>
4.8/5 - (5 votes)

Task 1: Overloading operators (5.0 marks)

A Euclidean vector is an array that consist n-tuples in a Euclidean space of dimension n.

It is very useful in mathematics, physics and engineering.

In this task, you will define a class EVector in a file EVector.h and implement the C++ program code in a file EVector.cpp.In the class EVector, declare a dynamic array of double type to store tuples for the

Euclidean vector, and declare an integer member to store the dimension of the vector. We will define and implement the following functions in the class EVector.• In the class EVector, you will define and implement default constructor, copyconstructor and other necessary constructors;• In the class EVector, you will define and implement overloading operators asfollowing:

o Extraction operator () to get input tuples’ values from keyboard;

o Insertion operator (&lt;&lt;) to print out the Euclidean vector tuples’ values;

o Assignment operator (=) to make a deep copy from another Euclideanvector object.

o Addition operation (+) to compute two Euclidean vectors’ addition. The addition of Euclidean vectors A (a1, …, an) + B (b1, …, bn) is defined as: C(c1, …, cn) = A(a1, …, an) + B(b1, …, bn), Where ci = ai+bi, i=1, …, n.

o Subtraction operation (-) to compute two Euclidean vectors’ subtraction.The subtraction of Euclidean vectors A (a1, …, an) – B (b1, …, bn) isdefined as: C(c1, …, cn) = A(a1, …, an) – B(b1, …, bn),where ci = ai-bi, i=1, …, n.

o Inner product operator (*) to compute two Euclidean vectors’ inner product. The inner product of Euclidean vectors A (a1, …, an) * B (b1, …, bn) is defined as:r = c1 + … + cn = A(a1, …, an) * B(b1, …, bn), where ci = ai * bi, i=1, …, n.

o Multiplication operator (*) to compute a Euclidean vector times a doublevalue. The multiplication of a Euclidean vector A (a1, …, an) * b is definedas:C( c1, …, cn) = A(a1, …, an) *b, where ci = ai * b, i=1, …, n.

o Multiplication operator (*) to compute a double value times a Euclideanvector. The multiplication of a Euclidean vector b * A (a1, …, an) isdefined as:C( c1, …, cn) = b * A(a1, …, an) ,where ci = b * ai, i=1, …, n.o Division operator (/) to compute a Euclidean vector divided by a doublevalue. The division of a Euclidean vector A (a1, …, an) / b is defined as:C( c1, …, cn) = A(a1, …, an) / b,where ci = ai/ b, i=1, …, n.

Implement a function main() in a file task1Main.cpp to test the functions / operators that defined above (See the Testing of the task for more details).Testing:

Use g++ to compile the source files on banshee by$ g++ –o task1 task1Main.cpp EVector.cpp

You can test the task by using the data defined in a text file input1.txt by$ ./task1 and input data that required. You program will print out results like following (Red data means input from keyboard):Input dimension and tuples for a Euclidean vector v1: 512.5 4.2 15.7 21.4 6.3

Euclidean vector v1 = (12.5, 4.2, 15.7, 21.4, 6.3)Input dimension and tuples for a Euclidean vector v2: 54.5 23.8 9.2 17.1 15.4Euclidean vector v2 = (4.5, 23.8, 9.2, 17.1, 15.4)v3 = v1 + v2 = (17, 28, 24.9, 38.5, 21.7)v3 = v1 – v2 = (8, -19.6, 6.5, 4.3, -9.1)v3 = v1 * v2 = 763.61Input a double value for d: 4d * v1 = 4 * (12.5, 4.2, 15.7, 21.4, 6.3) = (50, 16.8, 62.8, 85.6, 25.2)v1 * d = (12.5, 4.2, 15.7, 21.4, 6.3) * 4 = (50, 16.8, 62.8, 85.6, 25.2)v1 / d = (12.5, 4.2, 15.7, 21.4, 6.3) / 4 = (3.125, 1.05, 3.925, 5.35, 1.575)

You may run the program like:$ ./task1 &lt; input1.txt

To check memory leak, you may run the program by$ bcheck ./task1 &lt; input1.txt

You can download input data files input1.txt, input2.txt and input3.txt for your testing.Note: For addition, subtraction and inner product of two different dimensions ofEuclidean vectors, error messages should be prompted (such as “two Euclideanvectors should be in the same Euclidean space”), empty EVector objects (dimension zero, no tuple memory has been allocated) should be obtained; other operators should be fine.Note: Your program should work on different testing data files. There should be NO memory leak.

Task2: Class inheritance (5.0 marks)

In this task, we will define and implement inheritance classes.

Define the diagrams of the classes for bills below.

Define a base class Bill in a file Bill.h that contains biller’s name, code, referencenumber, account number, account name, address, amount due, totalGST, due date, period start date and period end date. Define necessary constructors, destructor, member functions and extraction operator () and insertion operator (&lt;&lt;) for the base class.

Implement the member functions and other friend functions in a file Bill.cpp.

Define a derived class ElectricityBill in a file ElectricityBill.h according to the diagrams above. Implement the functions in a file ElectricityBill.cpp. Define and implement overloading extraction operator () and insertion operator (&lt;&lt;) for the ElectricityBill class. Note the rates (rate1 $0.245/kWh, rate2 $0.264/kWh), threshold (1750 kWh) and supply charge ($0.699/day) are the same for all ElectricityBill instances.
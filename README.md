public class Mobile
{
    void iphone(){
        System.out.println("This is iphone");
    }
    void samsung(){
        System.out.println("This is Samsung phone");
    }

    public static void main(String[] args) {
        Mobile obj1=new Mobile();
        obj1.iphone();
        Mobile obj2=new Mobile();
        obj2.samsung();
    }
}

import java.util.Scanner;
public class Garden {
    float apple_price;
    int apple_count;

    void total(){
        System.out.println(apple_price*apple_count);
    }

    public static void main(String[] args) {
        Garden obj1=new Garden();
        Scanner scan=new Scanner(System.in);
        System.out.println("Input price of an apple:");
        obj1.apple_price=scan.nextFloat();
        System.out.println("Input count of apple:");
        obj1.apple_count=scan.nextInt();
        obj1.total();
    }
}

public class Store {
    void getsoap(int money)
    {
        System.out.print(money+" ");
        System.out.println("Soap purchased");
    }
    void getpowder(int amount)
    {
        System.out.print(amount+" ");
        System.out.println("powder purchased");
    }
    void getchocolates(int amount)
    {
        System.out.print(amount+" ");
        System.out.println("chocolate purchased");
    }
    public static void main(String[] args) {
        Store obj1=new Store();
        obj1.getsoap(20);
        obj1.getpowder(50);
        obj1.getchocolates(100);
    }
}

public class Sum {
    void add(int n1,int n2)
    {
        System.out.print("Total is:");
        System.out.println(n1+n2);
    }
    void multiply(int n1,int n2)
    {
        System.out.print("Multiplication is:");
        System.out.println(n1*n2);
    }

    public static void main(String[] args) {
        Sum obj1=new Sum();
        obj1.add(20,40);
        obj1.multiply(50,60);
    }
}

public class Name {
    public String getName() {
        return "kajananan";
    }

    public static void main(String[] args) {
        Name obj1 = new Name();

        String myName = obj1.getName();

        System.out.println(myName);
    }
}

import java.util.Scanner;
public class Find {
    int a;
    void find(){
        if(a%2==0){
            System.out.println("Even number");
        }else {
            System.out.println("Odd number");
        }
    }

    public static void main(String[] args) {
        Find obj1=new Find();
        Scanner scanner=new Scanner(System.in);
        System.out.println("Enter a value for a:");
        obj1.a=scanner.nextInt();
        obj1.find();
    }
}

public class School {
    void sum(int a,int b){
        System.out.println(a+b);
    }
    void sum(int a,int b,int c){
        System.out.println(a+b+c);
    }

    public static void main(String[] args) {
        School obj1=new School();
        obj1.sum(5,15);
        obj1.sum(5,15,25);
    }
}

class Animal{
    String name;
    int age;
    void makeSound(){
        System.out.println("Animal Makes Sound");
    }
}
class Dog extends Animal{
    String breed;

    @Override
    void makeSound() {
        System.out.println("Dog barks");
    }
    void fetch(){
        System.out.println("Dog is fetching");
    }
}
class Cat extends Animal{
    String colour;

    @Override
    void makeSound() {
        System.out.println("cat meows");
    }
    void climb(){
        System.out.println("Cat is climbing");
    }
}
public class Kingdom {
    public static void main(String[] args) {
        Animal a1=new Animal();
        a1.makeSound();
        a1.name="Dog";
        a1.age=5;
        Dog d1=new Dog();
        d1.makeSound();
        d1.fetch();
        Cat c1=new Cat();
        c1.colour="black";
        c1.makeSound();
        c1.climb();

    }
}

class VehicleBase { 
    String brand;
    int year;

    void startEngine() {
        System.out.println("This is a vehicle");
    }
}

class Car extends VehicleBase { 
    String fuelType;

    @Override
    void startEngine() {
        System.out.println("Car engine starts");
    }

    void drive() {
        System.out.println("Car is driving");
    }
}

class Truck extends VehicleBase { 
    int loadCapacity;

    @Override
    void startEngine() {
        System.out.println("Truck engine starts");
    }

    void haul() {
        System.out.println("Truck is hauling");
    }
}

public class Vehicle { 
    public static void main(String[] args) {
        Truck t1 = new Truck();
        t1.startEngine(); 
    }
}

package package_one;
import package_two.Teacher;
class Teacher1{
    private String name="praveen";
    void disp(){
        System.out.println(name);
    }
}

public class Student2 {
    public static void main(String[] args) {
        Teacher1 t1=new Teacher1();
        t1.disp(); 
        //System.out.println(t1.name); it will make an error because private class cant be accessible from out side
    }
}
// a private function only can be accessible inside a class

//Static keyword learning
package package_two;
class Student{
    static int mark=0;
}
public class Student1 {
    public static void main(String[] args) {
        Student s1=new Student();
        s1.mark=50;
        Student s2=new Student();
        s2.mark=100;
        System.out.println(s1.mark);
        //Output will always display the last updated value because of static key word,
    }
}

class Person{
    public String name;
    protected int age;
    private String socialsecuritynumber;
    String address;

    Person(String name, int age, String ssn, String address){
        this.name=name;
        this.age=age;
        this.socialsecuritynumber=ssn;
        this.address=address;
    }

}
class Employee extends Person {
    Employee(String name,int age,String ssn,String address){
        super(name,age,ssn,address);
        System.out.println("Hello Employee");
    }
}
public class Main {
    public static void main(String[] args) {
        Employee e1=new Employee("john",23,"xyz","chenni");
        System.out.println(e1.name);
        System.out.println(e1.age);
        System.out.println(e1.address);
       // System.out.println(e1.socialsecuritynumber);
    }
}
//john
//23
//chenni

class Counter{
    static int count=0;
    int instanceNumber=0;
    Counter(){
        count=count+1;
        instanceNumber=instanceNumber+1;
    }
    void disp(){
        System.out.println("InstanceNumber:"+instanceNumber);
        System.out.println("SystemCount:"+count);
    }
}
public class Mainclass {
    public static void main(String[] args) {
        Counter c1=new Counter();
        Counter c2=new Counter();
        Counter c3=new Counter();
        c1.disp();
        //1
        //3
        c2.disp();
        //1
        //3
        c3.disp();
        //1
        //3
       //Counter c1=new Counter();
        // c1.disp();
        //1
        //1
       //Counter c2=new Counter();
        // c2.disp();
        //2
        //1
        // Counter c3=new Counter();
        // c3.disp();
        //3
        //1
    }
}

interface playable{
    void play();
}
class guittar implements playable{
    public void play(){
        System.out.println("play guittar");
    }
}
class piano implements playable{
    public void play(){
        System.out.println("play piano");
    }
}
public class Inst {
    public static void main(String[] args) {
        guittar g1=new guittar();
        g1.play();
        piano p1=new piano();
        p1.play();
    }
}

import java.util.Scanner;
class DivisionExample{
    void dividenumbers(int num,int den){
        try{
             double result=num/den;
            System.out.println("Result is :"+result);
        }
        catch(ArithmeticException e){
            System.err.println("Cannot divisible by Zero");
        }
    }
}

public class Main {
    public static void main(String[] args) {
    DivisionExample d1=new DivisionExample();
    Scanner scan=new Scanner(System.in);
        System.out.println("Enter numerator :");
        int num=scan.nextInt();
        System.out.println("Enter denominator :");
        int den= scan.nextInt();
        d1.dividenumbers(num,den);
    }

}

class A extends Thread{
    public void run(){
        for(int i=0;i<5;i++){
            System.out.println("Hi");
        }
    }
}
class B extends Thread{
    public void run(){
        for(int i=0;i<3;i++){
            System.out.println("Hello");
        }
    }
}
public class Threaddd {
    public static void main(String[] args) {
        A a1=new A();
        B b1=new B();
        a1.setPriority(1);
        b1.setPriority(10);
        a1.start();
        b1.start();
    }
}

class cal{
    void div() throws Exception{
        int a=10/0;
        System.out.println(a);
    }
}
public class exce {
    public static void main(String[] args) {
        cal c1=new cal();
        try {
            c1.div();
        }
        catch (Exception e){
            System.out.println(e);
        }
    }
}

import java.util.InputMismatchException;
import java.util.Scanner;
class InvalidAgeException extends Exception{
    public InvalidAgeException(String message){
        super(message);
    }
}
class AgeValidator{
    void checkage(int age) throws InvalidAgeException {
            if (age <= 0 || age > 150) {
                throw new InvalidAgeException("Age is Invalid");
            }
            System.out.println("Age is valid:" + age);
    }
}
public class AgeException {
    public static void main(String[] args) {
        Scanner scan=new Scanner(System.in);
        try {
            System.out.println("Enter an age :");
            int age = scan.nextInt();
            AgeValidator a1 = new AgeValidator();
            a1.checkage(age);
        }catch(InputMismatchException e){
            System.out.println("Invalid input");
        }catch (InvalidAgeException e){
            System.out.println(e.getMessage());
        }catch (Exception e){
            System.out.println("unexpected error"+e.getMessage());
        }finally {
            scan.close();
        }
    }
}

import java.time.*;
public class Timelap {
    public static void main(String[] args) {
       LocalDate d=LocalDate.now();
        System.out.println(d);
    }
}









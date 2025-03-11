//Person
public class Person {
    String name;
    int age;

    public Person(String name) {
        this.name = name;
        this.age = 18;
    }

    public void displayInfo() {
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
    }

    public static void main(String[] args) { // Corrected main method signature
        Person person1 = new Person("Alice"); // Using the Person class
        person1.displayInfo(); // Calling a method of the Person class
    }
}

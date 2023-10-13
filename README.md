# Inheritance-explanation-in-JS-using-super-keyword-
This is a practical example  demonstrating inheritance using the super keyword 

___ SUMMARY ___ [In this example, we have an Animal class with a name property and a makeSound method. The Cat class extends Animal and adds a color property. By using the super(name) call in the Cat class constructor, we ensure that the name property is correctly initialized in both the Animal and Cat instances. This allows myCat to inherit the makeSound method from Animal while having its own purr method.]

    <script>
  
 class Animal {
  constructor(name) {
    this.name = name;
  }

  makeSound() {
    console.log(this.name + " makes a sound");
  }
}

class Dog extends Animal {
  constructor(name, color) {
    super(name); // Call the parent class constructor with the name
    this.color = color;
  }

  woof() {
    console.log(this.name + " barks");
  }
}

// Create objects of both the classes
const myAnimal = new Animal("Generic Animal");
myAnimal.makeSound();

const myDog = new Dog("Leo", "Black");
myDog.makeSound();
myDog.woof();

    </script>


Here our output will be --> 
Generic Animal makes a sound
Leo makes a sound
Leo barks

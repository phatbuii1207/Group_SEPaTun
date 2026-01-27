PROJECT PROPOSAL

Project Title: Pet Store Management System

2️⃣ Objectives (Mục tiêu)

Apply OOP concepts: Encapsulation, Inheritance, Polymorphism, and Abstraction.

Practice class design and object interaction.

Build a menu-driven program with validation and user interaction.

Manage data using collections (ArrayList).

3️⃣ System Features (Chức năng hệ thống)

Add new pets (Dog, Cat).

Remove pets.

Search pets by name.

Display all pets.

Create customer orders.

Calculate and display order total.

Exit the program safely.

4️⃣ Class Design (Thiết kế các class)
🔹 1. Class Pet (Base Class)

Role: Represents a general pet.

Attributes:

id, name, age, price, type

Methods:

input(): Input pet information.

display(): Display pet information.

getId(), getPrice(): Access data safely.

OOP:
Encapsulation, Abstraction, Parent class for inheritance.

🔹 2. Class Dog (Child Class)

Role: Represents a dog, extends Pet.

Attributes:

breed

Methods:

Override input() and display().

OOP:
Inheritance, Polymorphism.

🔹 3. Class Cat (Child Class)

Role: Represents a cat, extends Pet.

Attributes:

color

Methods:

Override input() and display().

OOP:
Inheritance, Polymorphism.

🔹 4. Class Customer

Role: Stores customer information.

Attributes:

id, name, phone

Methods:

input(), display()

OOP:
Encapsulation, Abstraction.

🔹 5. Class Order

Role: Represents a customer order.

Attributes:

orderId, customer, petList, totalAmount

Methods:

addPet(Pet p)

calculateTotal()

display()

OOP:
Polymorphism (Pet list), Encapsulation.

🔹 6. Class PetStoreManagement

Role: Manages pets and orders.

Attributes:

ArrayList<Pet> pets

ArrayList<Order> orders

Scanner sc

Methods:

addPet()

removePet()

searchPetByName()

displayAllPets()

createOrder()

OOP:
Abstraction (central control), Polymorphism.

🔹 7. Class Main

Role: Entry point and menu controller.

Methods:

main(): Displays menu, handles user input, and calls functions from PetStoreManagement.

OOP:
Abstraction (user interacts only with menu).

5️⃣ OOP Principles Applied
Principle	How It Is Applied
Encapsulation	Private/protected attributes, accessed via methods
Inheritance	Dog and Cat extend Pet
Polymorphism	Pet p = new Dog(); p.display();
Abstraction	Users interact through menu without knowing internal logic

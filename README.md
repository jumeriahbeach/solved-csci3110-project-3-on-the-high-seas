Download Link: https://assignmentchef.com/product/solved-csci3110-project-3-on-the-high-seas
<br>
File(s) to be submitted: ship.h, ship.cpp,cruiseship.h, cruiseship.cpp, cargoship.h,cargoship.cpp, proj3.cpp, makefileObjectives: 1) Use inheritance to derive new classes; 2) Understand abstract base classes; 3) Overload base classfunctions; 4) Override base class virtual functions; 5) Define base class pure virtual functions; 6) Understandstatic and dynamic function call binding; 7) Use custom destructors to free dynamically allocated memoryProject description:In this assignment you will create a class representing a ship, and two additional classes that inherit from the Ship class,a CargoShip class and a CruiseShip class. The project is geared toward giving you practical experience withcharacteristics and C++ implementation details of inheritance and polymorphism.Requirements:1. Your program must be split into 7 files. There will be 3 classes (each with separate interface and implementationfiles), and a driver file. The requirements for these are specified below:a) The Ship class – This is an abstract class Files must be named ship.h and ship.cpp Class must be named Ship Must contain #include guards for SHIP_H Will have these protected membersi. A string containing the ship’s nameii. A double representing the amount of fuel on board (in tons) Must have these public membersi. A two parameter constructor that takes the ship’s name and fuel load (in that order)ii. A parameterless void function, fuel, that outputs the ship’s name and its fuel load (see sample output)iii. A virtual void function, sail, that prints the ship’s name followed by the word “sailing” (see output)iv. A pure-virtual void function, load, that has a single integer parameter, and simulates loading the shipwith tonnage (cargo) or passengers (cruise)b) The CruiseShip class – This is a derived class that inherits from the Ship class as public Files must be named cruiseship.h and cruiseship.cpp Class must be named CruiseShip Must contain #include guards for CRUISESHIP_H Will have these private membersi. Three doubles that indicate the percentage of passengers in Luxury, Upper Deck, and Lower Deckcabins respectively. These values must sum to 1.ii. Three integers that indicate the number of passengers in Luxury, Upper Deck, and Lower Deck cabinsrespectively. Must have these public membersi. A five parameter constructor that takes the ship’s name, fuel load, and the percentages of passengersin Luxury, Upper Deck, and Lower Deck (in that order) – The percentages must sum to 1 – Thisconstructor must pass parameters to the constructor in the base classii. A void function, sail, that overrides the virtual function in the base class, and prints the ship’s nameand the number of passengers in Luxury, Upper Deck, and Lower Deck, in that order (see output)iii. A void function, load, that overrides/implements the pure virtual function in the base class, acceptsan integer representing the number of passengers as a parameter, and distributes those passengersamong the three cabin levels (Luxury, Upper Deck, Lower Deck) per the percentages specifiedc) The CargoShip class – This is a derived class that inherits from the Ship class as public Files must be named cargoship.h and cargoship.cpp Class must be named CargoShip Must contain #include guards for CARGOSHIP_H Will have these private membersi. Two double pointer variables to represent tonnage in the forward cargo bay and the aft cargo bayii. An integer that indicates the maximum total cargo capacity for the ship (in tons)iii. A double for the decimal percentage of cargo that is loaded in the forward bay Must have these public membersi. A four parameter constructor that takes the ship’s name, fuel load, cargo capacity, and forward baypercentage (in that order) – This constructor must pass parameters to the base class constructor andshould dynamically allocate the memory to represent the cargo bays and initialize them to zeroii. A destructor that frees the memory allocated for the cargo baysiii. A void function, fuel, that overloads the function in the base class, and has an integer parameter thatrepresents the fuel flashpoint – This function calls the fuel function in the base class, and also outputsits integer parameter, without any error checking or processing (see sample output)iv. A void function, load, that overrides/ implements the pure virtual function in the base class, acceptsan integer representing the tons of cargo to be loaded on the ship – A check must be made to ensurethat the ship is only loaded up to its capacity (if an overload is attempted, simply load to the maximumcapacity – do not output an error message) – This function should place a percentage of the cargo inthe forward bay (as specified in the input file) and the remainder in the aft bay, and should output theforward bay load and the aft bay load unformatted, in that order, on a single line (see sample output)c) A driver, or client, file Must be named proj3.cpp Must have two functions as shown below – main must be defined firsto sailShip – This void function simulates the ship getting underway with a single function call It has a single parameter: a reference to a Ship object It invokes the sail function through this objecto main – This function performs Must be defined first Opens and reads an input file named ships.txt, in this format (see sample input file): Line 1: Information about a cruise ship, in this order: ship name (a single word); fuelload (double); Luxury percentage; Upper Deck percentage; and Lower Deckpercentage (these 3 decimal percentages are doubles and must sum to 1); and thenumber of passengers to load (integer) Line 2: Information about a cargo ship, in this order: ship name (a single word); fuelload (double); Total Cargo capacity (integer); Forward Cargo Bay percentage (adouble) – (Note: the Aft Cargo Bay will hold 1 minus the Forward Bay percentage);cargo tonnage to load (integer); and Fuel flashpoint (integer) Instantiates a CruiseShip object with the information from the input file, and invokes its fuel,and load functions, and the sailShip function (with the CruiseShip object as an argument) Instantiates a CargoShip object and invokes its fuel, and load functions, and the sailShipfunction (with the CargoShip object as an argument)2. Sample output (based on sample input file provided with this assignment) – Your output must match. Do not addadditional verbiage, or change line spacing or character spacing (do not use tabs – only a single space between items):3. Test your program – Use different input files.4. Code comments – Add the following comments to your code: A section at the top of the source file(s) with the following identifying information:Your NameCSCI 3110-00X (your section #)Project #XDue: mm/dd/yy Below your name add comments in each file that gives an overview of the program or class. Place a one or two line comment above each function that summarizes the workings of the function.5. RubricRequirement Points OffShip ClassClass name -5Include guards -3Protected members -2 (per member)Constructor – number, types, and order of parameters -10Constructor – members correctly initialized -5 (per member)fuel – correct function signature -5fuel – correct output -5sail – correct function signature -5sail – correct output -5load – correct function signature -5CruiseShip ClassClass name -5Include guards -3Constructor – number, types, and order of parameters -10Constructor – correct call to base class constructor -5Constructor – derived class members correctly initialized -5Cabin percentages – private and sum to one -5Cabin number of passengers – private -5sail – correct function signature -5sail – correct output -5load – correct function signature -5load – correct implementation for distributing passenger to cabins -5CargoShip ClassClass name -5Include guards -3Private members declared/initialized per the specification -5Constructor – number, types, and order of parameters -10Constructor – correct call to base class constructor -5Constructor – memory correctly allocated -10Constructor – derived class members correctly initialized -5Destructor – explicitly deallocates memory used for cargo bay tonnage -10fuel – correct function signature to overload function in base class -5fuel – correct output -5load – correct function signature -5load – correctly handles attempts to add cargo beyond capacity -5load – correct implementation for distributing tonnage to cargo bays -5Driver/ClientsailShip – correct function signature -10sailShip – correctly invokes sail function -5main – Defined first -5main – Input filename -5main – Correctly reads input file -5main – Correctly instantiates CruiseShip and CargoShip objects (each object)main – Defined first -5main – Correctly invokes each object’s fuel function -5main – Correctly invokes each object’s load function -5main – Correctly invokes the sailShip function with each object as argument -10general – Does not compile (on ranger using Linux g++ compiler, and the provided makefile) -25general – Runtime crash -25general – Other TBD
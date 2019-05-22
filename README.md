# NaiveTicket

The second Objects lab, from the BlueJ book's second chapter.

Look for the [Chapter 2 file](./doc/BlueJ-objects-first-ch2.pdf) you need in the [doc](./doc) folder.
There is 35 pages of reading and exercises in the chapter.

Work through all these exercises. You edit this file with your answers for these exercises.

### Exercise 2.1
* Create a TicketMachine object on the object bench.
* Upon viewing its methods, `getBalance`, `getPrice`, `insertMoney`, `printTicket`.
* Use `getPrice` method to view the value of the price of the tickets that was set when this object was created.
* Use `insertMoney` method to simulate inserting an amount of money into the machine.
* Use `getBalance` to check that the machine has a record of the amount inserted.
	* You can insert several separate amounts of money into the machine, just like you might insert multiple coins or notes into a real machine. Try inserting the exact amount required for a ticket. As this is a simple machine, a ticket will not be issued automatically, so once you have inserted enough money, call the `printTicket` method. A facsimile ticket should be printed in the BlueJ terminal window.

### Exercise 2.2
* What value is returned if you check the machine’s balance after it has printed a ticket?
0

### Exercise 2.3
* Experiment with inserting different amounts of money before printing tickets.
	* Do you notice anything strange about the machine’s behavior?
	The ticket always prints wether you insert money or not.

	* What happens if you insert too much money into the machine – do you receive any refund?
	nope, the balance will return to 0.

	* What happens if you do not insert enough and then try to print a ticket?
	It still prints ticket!

### Exercise 2.4
* Try to obtain a good understanding of a ticket machine’s behavior by interacting with it on the object bench before we start looking at how the `TicketMachine` class is implemented in the next section.

### Exercise 2.5
* Create another ticket machine for tickets of a different price.
	* Buy a ticket from that machine.
	* Does the printed ticket look different?
	The price is different.

### Exercise 2.6
* Write out what you think the outer wrappers of the `Student` and `LabClass` classes might look like – do not worry about the inner part.
public class Student {...}
public class LabClass {...}

### Exercise 2.7
Does it matter whether we write<br>
`public class TicketMachine`<br>
or<br>
`class public TicketMachine`<br>
in the outer wrapper of a class?

* Edit the source of the `TicketMachine` class to make the change and then close the editor window.
	* Do you notice a change in the class diagram?
	The grey line become red cross line because there is error in the code.
	* What error message do you get when you now press the compile button?
	<identifier> expected
	* Do you think this message clearly explains what is wrong?
	not really..

### Exercise 2.8
* Check whether or not it is possible to leave out the word `public` from the outer wrapper of the `TicketMachine` class.
Yes we can.

### Exercise 2.9
* From your earlier experimentation with the ticket machine objects within BlueJ you can probably remember the names of some of the methods – `printTicket`, for instance.
	* Look at the class definition in Code 2.1 and use this knowledge, along with the additional information about ordering we have given you, to try to make a list of the names of the fields, constructors, and methods in the `TicketMachine` class.
	* Hint: There is only one constructor in the class.
Fields:
int price
int balance
int total

Constructors:
public TicketMachine(int ticketCost)

Methods:
public int getPrice()
public int getBalance()
public void insertMoney(int amount)
public void printTicket()


### Exercise 2.10
* Do you notice any features of the constructor that make it significantly different from the other methods of the class?
There is no return type, and it's name must be the same as the class.

### Exercise 2.11
* What do you think is the type of each of the following fields?

```java
private int count;
private Student representative;
private Server host;
```
type int, type Student, type Server

### Exercise 2.12
* What are the names of the following fields?

```java
private boolean alive;
private Person tutor;
private Game game;
```
alive, tutor, game

### Exercise 2.13

In the following field declaration from the TicketMachine class<br>

```java
private int price;
```
does it matter which order the three words appear in?
* Edit the `TicketMachine` class to try different orderings. After each change, close the editor.
	* Does the appearance of the class diagram after each change give you a clue as to whether or not other orderings are
possible?
	* Check by pressing the compile button to see if there is an error message.
	* Make sure that you reinstantiate the original version after your experiments!
There is no difference.

### Exercise 2.14
* Is it always necessary to have a semicolon at the end of a field declaration?
* Once again, experiment via the editor.
* The rule you will learn here is an important one, so be sure to remember it.
BIG YES! That's how the compiler know where that line of code stops. 

### Exercise 2.15
* Write in full the declaration for a field of type `int` whose name is `status`.
int status;

### Exercise 2.16
* To what class does the following constructor belong?
```
public Student(String name)
```
class Student{...}

### Exercise 2.17
* How many parameters does the following constructor have and what are their types?
```
public Book(String title, double price)
```
2, type String and type double

### Exercise 2.18
* Can you guess what types some of the `Book` class’s fields might be?
There will be at least type String and type double.

* Can you assume anything about the names of its fields?
It should be called something like bookTitle and bookPrice.

Work all Exercises from 2.19 to 2.58 that are **NOT** marked *Challenge exercise*.

2.19
name = petsName;

2.21
one returns price and the other returns balance.

2.22
How much is my Balance?

2.23
Nope.

2.24
public int getTotal()
{
    return total;
}

2.25
Missing return statement

2.26
one is int and one is void.

2.27
Nope! Because void methods does not need a return statement, the methods thus return nothing.

2.29
It's header has void type.

2.30
public void setPrice(int ticketCost)
{
    price = ticketCost;
}

2.31
public void increase(int points)
{
    score += points;
}

2.32
public void discount(int amount)
{
    price -= amount;
}

2.33
public void prompt()
{
    System.out.println("Please insert the correct amount "
    + "of money");
}
2.34
    public void showPrice()
    {
        System.out.println("The price of a ticket is " + price 
        + " cents.");
    }
2.35
yes they are different, because the price field is different.

2.36
It will print "# price cents.", not the cotent of price field.

2.37
Still "# price cents."

2.38
Nope! It will only print literal word "price".

2.39
It stops asking for price of the ticket.

2.40
This method is a mutator because it alters the field in the object.

2.41
Yes! It's a mutator.

2.42
public TicketMachine(int ticketCost)
{
    price = ticketCost;
    balance = 0;
    total = 0;
}
public TicketMachine()
{
    price = 1000;
    balance = 0;
    total = 0;
}

2.43
Balance does not change when we give it garbage value.
But it will reduce balance given negative integer.

2.44
It will not change balance when we entered a negative amount.

2.45
bool isVisible is use to control whether or not the circle is displayed. It's well suited.

2.46
1. The insertMoney method stop user from entering a negative amount
2. The ticket will not print ticket when users don't have enough balance.
3. The machine will keep the remaining balance instead of eating it up.
4. The machine will refund the user with the remaining balance when invoke refundBlance method.

2.47
No, because balance = balance - price only happen when balance >= price, 
so balance will be 0 a minimum. 

2.48
there is also *, /, and %.

2.49
saving = price * discount;

2.50
mean = total / count;

2.51
if (price > budget)
    System.out.println("Too expensive");
else
    System.out.println("Just right");

2.52
if (price > budget)
    System.out.println("Too expensive! Budget: " + budget);
else
    System.out.println("Just right");

2.53
Since it set the balance to 0 right before it return it, it will always refund nothing.

2.54
It says "Unreachable statement"
because return will terminate the method, the statement after that won't run and it is useless.

2.55
public int emptyMachine()
{   
    int moneyBag = total;
    total = 0;
        
    return moneyBag;
}

2.56
Both!

2.57
public void printTicket()
{
    int amountLeftToPay = price - balance;
    if(amountLeftToPay <= 0) {
        // Simulate the printing of a ticket. 
        System.out.println("##################"); 
        System.out.println("# The BlueJ Line"); 
        System.out.println("# Ticket"); 
        System.out.println("# " + price + " cents."); 
        System.out.println("##################"); 
        System.out.println();
        // Update the total collected with the price.
        total = total + price;
        // Reduce the balance by the price.
        balance = balance - price;
    }
    else {
        System.out.println("You must insert at least: " +
                           amountLeftToPay + " cents.");
    } 
}

READ upto and INCLUDING section 2.15 of this chapter.

# lab04

All of these questions deal with the ticket machine example bundled in this repo. You should fork this repo and clone the fork to work on the code locally.

## How can we tell from just its header that `setPrice` is a method and not a constructor?
```
public void setPrice(int cost)
```
* One can tell from the header that `setPrice` is a method and not a constructor because the header because it has no output and its name does not match that of the class.

## Complete the body of the setPrice method so that it assigns the value of its parameter to the price field. Write your new method in the `lab04-ticket-machine`.

## Complete the body of the following method, whose purpose is to add the value of its parameter to a field named `score`.
```
/**
 * Increase score by the given number of points.
 */
public void increase(int points)
{
  score=score+points;
}
```
## Is the `increase` method in the previous question a mutator? If so, how could you demonstrate this?
* The `increase` method in the previous question is a mutator because it changes a parameter to the field `score`.

## Complete the following method, whose purpose is to subtract the value of its parameter from a field named `price`. Add your new method to the `lab04-ticket-machine`.
```
/**
 * Reduce price by the given amount.
 */
public void discount(int amount)
{
  price=price-amount;
}
```

## Write down exactly what will be printed by the following statement:
```
System.out.println("My cat has green eyes.");
```
* My cat has green eyes.

## Add a method called `prompt` to the `TicketMachine` class in the `lab04-ticket-machine`. This should have a `void` return type and take no parameters. The body of the method should print the following single line of output:
```
Please insert the correct amount of money.
```

## What do you think would be printed if you altered the fourth statement of `printTicket` so that `price` also has quotes around it, as follows?
```
System.out.println("# " + "price" + " cents.");
```
The system would print `# price cents.`

## What would be printed here?
```
System.out.println("# price cents.");
```
* The system would print `# price cents.`

## Could either of the previous two versions be used to show the price of tickets in different ticket machines? Explain your answer.

* Neither of the previous two versions could be used to show the price of tickets in different machines, as they print a String, "price", rather than the int `price`. Only the latter will show the actual price of the tickets when prompted.

## Add a `showPrice` method to the `TicketMachine` class in the `lab04-ticket-machine`. This should have a void return type and take no parameters. The body of the method should print (here `xyz` should be replaced by the value held in the `price` field when the method is called):
```
The price of a ticket is xyz cents.
```

## Create two ticket machines with differently priced tickets. Do calls to their showPrice methods show the same output, or different? How do you explain this effect?
* Two ticket machines with two different prices produce different outputs when the showPrice method is called. This behavior is due to the fact that the two machines are different instances of a class, and have different parameters for the int `price`, which determines the price displayed in the output of showPrice.

## Modify the constructor of `TicketMachine` in the `lab04-ticket-machine` so that it no longer has a parameter. Instead, the price of tickets should be fixed at 1,000 cents. What effect does this have when you construct ticket-machine objects within BlueJ?
* Modifying the constructor `TicketMachine` so it no longer has a parameter makes it so that all objects of the class `TicketMachine` produced by this code have the field `int price` fixed at 1000 cents.

## Give the class two constructors. One should take a single parameter that specifies the price, and the other should take no parameter and set the price to be a default value of your choosing. Test your implementation by creating machines via the two different constructors.

## Implement a method, `empty`, that simulates the effect of removing all money from the machine. This method should have a `void` return type, and its body should simply set the `total` field to zero. Does this method need to take any parameters? Test your method by creating a machine, inserting some money, printing some tickets, checking the total, and then emptying the machine. Is the `empty` method a mutator or an accessor?
* The method `empty` does not need to take any parameters, as it functions to always set total to the same amount (0). The `empty` method is a mutator, as it changes a field value (`total`) of an object.

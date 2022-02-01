# Agent-Based-Simulation
Book Trading simulation using agents. This project was part of my submitted assignments for the Distributed Intelligent Systems module as part of Msc AI and Data Science I was taking at Keele University.


**Book Trading Simulation**

The book trading simulation aims to simulate the behaviour of autonomous agents in a changing environment.
This project is about modeling a system that evolves over time, using a representation in which state variables can only change at a
countable number of points in time, called events. The system is composed of
agents (buyers, sellers and a broker), resources (books, time, money). The state variables
such as stock levels, availability of agents change at the occurrence of events (buy, sell).

**The stages of the buying process**

Need identification: The buyer becomes aware of the need to buy books, in this case, the user initiates
the request and the buyer agent carries it on behalf of the user.

Product and merchant brokering : The broker has all information about buyers and sellers, these two types of
agents do not communicate directly. The broker is also responsible for distributing the books
to sellers. This agent also retrieves information to decide which books to buy based on buyer request and price
 and availability of the requested book.

Purchase and delivery : signals termination of the buying process, update stock
and buyer's possessions.

**Books trading project in java**
The system is composed of the following classes:
-  Trading: Main simulation class, contains books initialization, creation of broker agent which then invokes buyers and sellers.
In this simulation, the buyers number is set to 1 as the requests are set to be made by the user in different intervals, 
having multiple buyer agents is not useful, however these can be created by the broker and the simulation process can be adapted
accordingly. User parameters are also set in this class (allocated budget). The main loop sets the user interface where the
user can input the title of the book they want to buy and then agents respond to the user's request.
 - Agent class: the main class for agent creation, it has one constructor method for defining general agent properties
as an object. In our case, only the ID is needed.
 - Seller class: each seller has a bookshelf that is filled at the start of the simulation and is updated at the 
occurrence of buy and sell events. The seller has the following methods: NewBook(), ShareListing(), and confirmSale().
 - Broker class: The broker is responsible for coordination between buyers and sellers. This agent can set the number of
sellers and buyers and has their ids stored in lists. The following methods can be called: collectOffer(), buy(), 
generateSellers(), distributeBooks().
 - Buyer class: buyer takes on the user's request. It has the following methods: requestBook() and buyBook().
 - Books class: This class defines the book object (id, title, price). This class has a constructor method books(), and 
setPrice() to update a book's price.

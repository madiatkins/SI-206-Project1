206 Project 1 - Code for playing cards.
README.txt



Your name:
 Madi Atkins
Anyone you worked with: N/A

----- Add your README file content for the Project 1 code.

-----

- What does this code do overall?
This code creates classes which allow users to create cards, decks, and hands in order to play a modified game of War. Additionally, the classes created in this code would allow a user to define new functions to create new card games.

- What does each class do? What does each method within each class do?

~NOTE: Each class builds off one another (i.e. Card() is necessary in running Hand()). If you were to remove one, you would need to edit the following class in order for the code to work correctly.

Card():
An instance of the class Card() represents a single card from a typical playing card deck. 

There are no required input to the class constructer. There are two optional input: suit and rank. For suit you may enter an integer 0 through 3 that will index through the suit_names list. For rank you may enter an integer 1 through 13 that will correspond to the rank_levels list. If you do not provide values for the input variables, then the default for each will be suit = 0 and rank = 2.

There is only one method other than the class constructer __init__ which is defined within the Card() class.
The method __str__() takes card rank and card suit (eg. "Jack" and "Clubs" or 3 and "Spades") and returns a formatted string that lists what each individual card created is (eg. "Jack of Clubs" or "3 of Spades").


Deck():
An instance of the class Deck() represents a typical 52-card deck of playing cards.

There are no required or optional input for the Deck() class.

There are 5 methods other than the class constructer __init__ which are defined within the Deck() class.
The method __str__() takes the list created by self.cards and returns a multi-line string listing each card in the deck.
The method pop_card() removes and returns a card from the deck (i.e. this card is no longer in the deck). The only input is optional - for 'i' you may input an integer to tell the program what location to pull the card from. The default is -1, or the last card in the deck.
The method shuffle() is pretty self-explanatory - uses the random module and it's method .shuffle() to shuffle the deck of cards and return that newly shuffled deck.
The method replace_card() takes a list of cards appends the card string (created by __str__() above) to the list card_strs. If that particular card string is not in card_strs, then it appends that card to the deck list of cards.
The method sort_cards() creates a list of cards which are sorted into tuples in order of (suit of card, rank of card) and appended to the list self.cards = []


Hand():
An instance of the class Hand() represents a single hand of playing cards (5 cards, but can be changed).

There is one required input and one optional input. You are required to input a deck of cards that the Hand() will use (in this case you would input deck_to_use = Deck(), unless you create a new, unique deck from this code to input). The optional input is how many cards you wish to have in your hand. If you do not input any number for this input variable, then the default for num_cards will be num_cards = 5. 
~NOTE: You may only have up to 26 cards in your hand at one time, so if you input an integer greater than 26, it will cause an error in the code. Feel free to mess around with the code in order to fix this bug!

There are 6 methods other than the class constructer __init__ which are defined within the Hand() class.
The method place_card() removes and returns a card from the cards in hand. Basically the same as pop_card from the Deck() class, but instead it's referencing the Hand() cards. Similar to pop_card() above, the only input is optional - for 'i' you may input an integer to tell the program what location to pull the card from. The default is -1, or the last card in the hand.
The method get_suits_available() returns a list of all the suits that are in the hand. No input.
The method get_ranks_available() returns a list of all the ranks taht are in the hand. No input.
The method specific_card() takes in two input - suit and rank - and if it finds the card with this suit and rank in the hand, it will remove that card from the hand and return it. If it does not find the card in the hand it returns a None value.
The method add_card() takes in one input - card - and adds the card to the hand if there is no identical one already there. Assumes you are working with one deck.
The method __str__() returns a multi-line string listing each card that is currently in the hand. No input.

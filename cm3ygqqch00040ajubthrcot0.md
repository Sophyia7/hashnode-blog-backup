---
title: "How to Create a Number-Guessing Game in Python"
seoTitle: "Number-Guessing Game: Python Guide"
seoDescription: "Learn to build a Python number-guessing game using loops, if-else statements, and random numbers with this beginner-friendly guide. "
datePublished: Tue Nov 26 2024 12:58:48 GMT+0000 (Coordinated Universal Time)
cuid: cm3ygqqch00040ajubthrcot0
slug: how-to-create-a-number-guessing-game-in-python
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1732625245486/a5ba5510-adc6-4a6a-aa82-d5941b734b28.png
tags: python, hashnode, python-beginner, python-projects

---

Hello there! 👋

In this guide, you will learn how to build a number-guessing game using basic Python concepts, such as loops, if-else statements, handling inputs, and more. This is inspired by the [Number guessing game project](https://roadmap.sh/projects/number-guessing-game) in the Roadmap projects section.

Let’s get started! 😎

## Creating the game’s function

We would need to create a function to handle the generation of the random number for the user to guess using Python’s `random` module.

Start by importing the module then create the function using `random.randint()` within the module to generate a random number between 1 - 100, this is the number the player has to guess and it will be stored in a variable, **number\_to\_guess**.

Next, set **guessed\_correctly** var to false to stop the game once the player guessed the right number and set an **attempts\_limit** to make the game more difficult.

```python
import random

def number_guessing_game(attempts_limit=7):
  number_to_guess = random.randint(1, 100)
  guessed_correctly = False
  attempts = 0
```

Next, use a print statement to welcome your player with some messages and instructions on how to play the game. You can customize this to your preference.

*NB: This should be within the function.*

```python
  print("Welcome to Number guessing game")
  print("I have selected a number from 1-100, can you guess it?")
```

## Creating the guessing loop

Next, we need to create the core of the game. This will manage the loop that continues until the player guesses the number correctly or reaches their guess limit.

Start by using a while loop to increase the attempt count with each try. If the player doesn't guess correctly, they should be given another turn to guess as long as they haven't exceeded their limit.

```python
  while attempts < attempts_limit and not guessed_correctly:
     guess = int(input("Please add your guess: "))
     attempts +=1
```

Next, use an if-else statement to compare the player's guess with the random number and provide feedback. If the guess is lower than the correct number, print "too low." If it's too high, print "too high." If it matches the correct number, set `guessed_correctly` to True, break the loop, and print a congratulations message.

```python
if guess < number_to_guess:
    print("Too low!")
elif guess > number_to_guess:
    print("Too high")
else:
    guessed_correctly = True
    print(f"Congratulations, you guessed the number in {attempts} attempts")
```

Next, let's add an extra layer of error handling. Users can be unpredictable, and many might try to break your program. For example, if a player decides to use a letter or a decimal number to guess, the program will stop unexpectedly. That's why we need this extra layer.

Using the try-except block, we can catch such an error. It should only accept whole numbers and should send an error message and stop if the player decides to use something else.

```python
  while attempts < attempts_limit and not guessed_correctly:
    try:
      guess = int(input("Please add your guess: "))
      attempts +=1

      if guess < number_to_guess:
        print("Too low!")
      elif guess > number_to_guess:
        print("Too high")
      else:
        guessed_correctly = True
        print(f"Congratulations, you guessed the number in {attempts} attempts")

    except ValueError:
      print("Oops! This is not a valid number, please a whole number")
```

Once that's done, we move on to the final step. If the player runs out of guesses and hasn't guessed the correct number, display a message saying "Game over" and inform them that they are out of guesses.

```python
  if not guessed_correctly:
    print(f"You are out of guesses, the correct guess was {number_to_guess}")
  
  print("Game over, Thanks for playing!")
```

## Testing your game

Now that’s all done! Let’s test our game and see if it works. Also, remember to call your function at the bottom of your program to run your program.

```python
number_guessing_game()
```

This is how your number-guessing game should look :

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1732458886302/571cab99-c6aa-40de-8f57-914207013c39.png align="center")

## Conclusion

And there you have it! A simple yet fun game in Python that you can create as a beginner. I hope this helps you become more comfortable with key programming concepts like loops, conditionals, and random numbers.

The source code can be found [here](https://github.com/Sophyia7/Python-Tutorials). If you prefer the video version of this guide, check it out:

%[https://youtu.be/MrTWan2td28?si=Sl0ssjckBu716n8m]
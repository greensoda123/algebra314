---
layout: post
title: "Why the Monty Hall Problem Still Feels Wrong"
date: 2026-03-20
---

The Monty Hall problem is interesting because it feels like the odds are 50/50, but it is not. Here is how it works:

- You choose 1 of 3 doors
- Behind 1 is a car
- Behind the other 2 are goats
- Your aim is to open the door with the car
- The host knows what door has what
- After you choose, the host opens a door with a goat from one of the 2 doors you did not choose
- Now you have the option to switch to the other unopened door
- Should you switch?

At first, it looks 50/50 because there are only 2 choices, but the chances of the door you did not pick having a car is 2/3. Here is why.

When the host opens a goat door from those two, that 2/3 probability does not disappear - it concentrates on the one remaining unopened door.

So:

- Probability your original choice was right: 1/3
- Probability the other unopened door is right: 2/3

That is why switching is better.

This took me a bit to properly understand, but a useful way to see this is to imagine 100 doors instead of 3. You pick 1 door, and the host opens 98 goat doors. It becomes much easier to see that your first choice is probably wrong, and that the one remaining unopened door is much more likely to contain the prize.

If you want to try this specific 100 door scenario for yourself, here is some Python code I made. After you play it a few times, you will start noticing how it is definitely not 50/50, and switching nearly always gives you a car.

```python
import random

def play_game():
    doors = list(range(1, 101))
    car = random.choice(doors)

    # Player picks a door
    while True:
        try:
            first_pick = int(input("Pick a door (1-100): "))
            if 1 <= first_pick <= 100:
                break
            else:
                print("Enter a number between 1 and 100.")
        except:
            print("Invalid input, try again.")

    print(f"\nYou picked door {first_pick}")

    # Determine the other unopened door
    if first_pick == car:
        # Picked correctly, then leave one random goat
        other_options = [d for d in doors if d != first_pick and d != car]
        other_door = random.choice(other_options)
    else:
        # Picked wrong -> other door must be the car
        other_door = car

    print("Host opens 98 doors... all goats")
    print(f"Remaining doors: {first_pick} and {other_door}")

    # Switch decision
    while True:
        switch = input("Do you want to switch? (yes/no): ").lower()
        if switch in ["yes", "no"]:
            break
        print("Type 'yes' or 'no'.")

    final_pick = other_door if switch == "yes" else first_pick

    # Result
    if final_pick == car:
        print("You got the CAR!")
    else:
        print("You got a goat.")

    print(f"(Car was behind door {car})")


# Game loop
while True:
    play_game()
    again = input("\nPlay again? (yes/no): ").lower()
    if again != "yes":
        break
```
What makes this problem interesting is not just the answer, but the fact that intuition pushes so strongly in the wrong direction. It is a good example of how mathematical reasoning can correct instinctive thinking.

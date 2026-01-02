---
title: "From Dream to Code: Guessing Game"
date: 2026-01-01 09:30:00 +0530
categories: [Blogging, Projects]
tags: [java, logic, threadlocalrandom]
---

## Waking Up and Coding

Hello everyone! I'm **Void Main**. This is a special entry because it wasn't planned. The idea for this project came to my mind last night before I slept. I kept thinking about the logic, slept with the idea, and the moment I woke up, I grabbed my laptop and started coding.

## The Number Guessing Game

The project is a classic Number Guessing Game. The computer picks a random number, and the user has to guess it with hints like "Too High" or "Too Low".

I didn't want to just use the standard `Random` class. I did some research and implemented **ThreadLocalRandom**, which is a more efficient way to generate numbers in modern Java.

```java
// Generating a number between 1 and 100
int randomNumber = ThreadLocalRandom.current().nextInt(1, 101);
```
I also focused on making the game "crash-proof". If a user enters text instead of a number, the program catches the error and clears the buffer so the game continues smoothly.

```java
try 
{
    int num = sc.nextInt();
    obj.Guess(num, randomNumber);
}
catch (Exception e)
{
    System.out.println("Please enter a number!");
    sc.nextLine(); // Clears the invalid input
}
```
You can find the complete source code on my [Github](https://github.com/VoidMain-01).

### Future Improvements

I am planning to add a counter to limit the number of attempts, making the game more challenging.

```java
System.out.println("Wishing everyone a Happy New Year");
```
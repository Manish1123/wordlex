# WordleX

WordleX is a clone of the popular online puzzle game, [Wordle](https://www.powerlanguage.co.uk/wordle/), forked from [word-mastermind](https://github.com/clupasq/word-mastermind).

It's like the board game, [MasterMind game](https://en.wikipedia.org/wiki/Mastermind_(board_game)), but instead of colors you have to guess words.

## Why?

* The online game only allows one word per day. WordleX can be played over and over.
* WordleX is self-hosted so you have complete control over the code - including the use of custom dictionary files.

## Demo

You can try it out on Glitch:

* [English](https://word-mastermind.glitch.me/)
* [Romanian](https://word-mastermind.glitch.me/?dictName=ro-ro-5)
* [Romanian (6 letter words)](https://word-mastermind.glitch.me/?dictName=ro-ro-6)
* [Swedish](https://word-mastermind.glitch.me/?dictName=sv-se-5)
* [Dutch](https://word-mastermind.glitch.me/?dictName=nl-nl-5)

## How to Play
(Note that WordleX has a "?" button above the playing board that displays the "How to Play" text.)

The goal of the game is to guess the 5-letter target word.

To do so, you enter guesses and the game will provide feedback that you can use for your next guess:

* An unmarked letter is not present in the target word.
* A letter marked in red is present in the target word but in the wrong spot.
* A letter marked in green is present in the target word and in the correct spot.

All submitted guesses have to be valid words found in a dictionary.

To help you with your next guess, the keyboard at the bottom of the screen will highlight the status of each letterthat you have used in your guesses.

## Running the program

Clone this repo:

```
git clone https://github.com/don-ferris/WordleX.git
cd WordleX
```

There are two options for runnning the program: with Node.JS or in Docker.

### Running with node

Make sure you have Node.JS 16 installed.

In the `WordleX` directory, install the dependencies using `yarn install` or `npm install`.

Run the server: `npm start`.

Go to http://localhost:3333.

### Running with Docker

In the `WordleX` directory, issue the following command to prepare the Docker image:

```
docker build -t WordleX .
```

Then run the image:

```
docker run --rm -p "3333:80" WordleX
```

Go to http://localhost:3333.

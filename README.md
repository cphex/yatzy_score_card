# Yatzy Score Card

Yatzy is a dice game where one to any number of players take turn rolling five dices. After the first roll the player can choose to keep or re-roll dices up to two times in a turn. A score must be put on the score card when the player has no more re-rolls; if the roll yielded a score of zero points one of the options must me sacrificed. The game ends when there are no more options on the score card. The player with the highest total score wins the game.

## The Yatzy Score Card

A Yatzy scores card looks like this:

| Name            | Description                                   | Score            | Example    | Max score |
| --------------- | --------------------------------------------- | ---------------- | ---------- | --------- |
| Ones            | The number of dice showing one eye            | Sum of ones      | 11123 =  3 |         5 |
| Twos            | The number of dice showing two eyes           | Sum of twos      | 22234 =  6 |        10 |
| Threes          | The number of dice showing three eyes         | Sum of threes    | 33345 =  9 |        15 |
| Fours           | The number of dice showing four eyes          | Sum of fours     | 14444 = 16 |        20 |
| Fives           | The number of dice showing five eyes          | Sum of fives     | 23555 = 15 |        25 |
| Sixes           | The number of dice showing six eyes           | Sum of sixes     | 24666 = 18 |        30 |
| One pair        | Two dice showing ones                         | Sum of the pair  | 11345 =  2 |        12 |
| Two pair        | Two different pairs of dice                   | Sum of the pairs | 11355 = 12 |        22 |
| Three of a kind | Three dice showing the same eyes              | Sum the eyes     | 12555 = 15 |        18 |
| Four of a kind  | Four dice showing the same eyes               | Sum the eyes     | 12222 =  8 |        24 |
| Small straight  | The combination 1-2-3-4-5                     | 15               | 12345 = 15 |        15 |
| Large straight  | The combination 2-3-4-5-6                     | 20               | 23456 = 20 |        20 |
| Full house      | Two of a kind combined with a three of a kind | Sum              | 33555 = 21 |        28 |
| Chance          | Any combination of dice                       | Sum              | 12234 = 12 |        30 |
| Yatzy           | Five dice with the same number of eyes        | 50               | 33333 = 50 |        50 |

## Exercise

Build a server using Elixir or Erlang that keep the state of a single Yatzy score card.

Note that this exercise does not involve keeping track of who's turn it is, nor does it involve creating dice throws. The focus is entirely on the state of one individual yatzy score card.

  - [ ] Create a process that can receive yatzy scores. The interface could look like `YatzyScoreCard.register(player, {:ones, 5})` where `player` is the `pid` or the process keeping the state.

  - [ ] The server should keep track of the options on the score card, which ones has been taken and with what score. It is okay to let the server crash if an invalid score has been given for a given score

  - [ ] The server should be able to return the total score of the score card

### Extra tasks

  - [ ] Make it possible to spawn and track more than one score card

  - [ ] Create a supervisor and respawn processes if they die (`Process.exit/2` can be used in tests)

## How to get started

Fork this repository to your own GitHub account. This will allow us to compare solutions using [the forks view for this project on Github](https://github.com/cphex/enum_workshop/network).

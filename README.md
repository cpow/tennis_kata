## Tennis Kata

Tennis has a rather quirky scoring system, and to newcomers it can be a little difficult to keep track of. The tennis society has contracted you to build a scoreboard to display the current score during tennis games.

Your task is to write a “TennisGame” class containing the logic which outputs the correct score as a string for display on the scoreboard. When a player scores a point, it triggers a method to be called on your class letting you know who scored the point. Later, you will get a call “score()” from the scoreboard asking what it should display. This method should return a string with the current score.

You can read more about Tennis scores [here](http://en.wikipedia.org/wiki/Tennis#Scoring) which is summarized below:

1. A game is won by the first player to have won at least four points in total and at least two points more than the opponent.
2. The running score of each game is described in a manner peculiar to tennis: scores from zero to three points are described as "Love", "Fifteen", "Thirty", and "Forty" respectively.
3. If at least three points have been scored by each player, and the scores are equal, the score is "Deuce".
4. If at least three points have been scored by each side and a player has one more point than his opponent, the score of the game is "Advantage" for the player in the lead.

You need only report the score for the current game. Sets and Matches are out of scope.
```
TEST_CASES = [
  [0, 0, "Love-All", 'player1', 'player2'],
  [1, 1, "Fifteen-All", 'player1', 'player2'],
  [2, 2, "Thirty-All", 'player1', 'player2'],
  [3, 3, "Deuce", 'player1', 'player2'],
  [4, 4, "Deuce", 'player1', 'player2'],

  [1, 0, "Fifteen-Love", 'player1', 'player2'],
  [0, 1, "Love-Fifteen", 'player1', 'player2'],
  [2, 0, "Thirty-Love", 'player1', 'player2'],
  [0, 2, "Love-Thirty", 'player1', 'player2'],
  [3, 0, "Forty-Love", 'player1', 'player2'],
  [0, 3, "Love-Forty", 'player1', 'player2'],
  [4, 0, "Win for player1", 'player1', 'player2'],
  [0, 4, "Win for player2", 'player1', 'player2'],

  [2, 1, "Thirty-Fifteen", 'player1', 'player2'],
  [1, 2, "Fifteen-Thirty", 'player1', 'player2'],
  [3, 1, "Forty-Fifteen", 'player1', 'player2'],
  [1, 3, "Fifteen-Forty", 'player1', 'player2'],
  [4, 1, "Win for player1", 'player1', 'player2'],
  [1, 4, "Win for player2", 'player1', 'player2'],

  [3, 2, "Forty-Thirty", 'player1', 'player2'],
  [2, 3, "Thirty-Forty", 'player1', 'player2'],
  [4, 2, "Win for player1", 'player1', 'player2'],
  [2, 4, "Win for player2", 'player1', 'player2'],

  [4, 3, "Advantage player1", 'player1', 'player2'],
  [3, 4, "Advantage player2", 'player1', 'player2'],
  [5, 4, "Advantage player1", 'player1', 'player2'],
  [4, 5, "Advantage player2", 'player1', 'player2'],
  [15, 14, "Advantage player1", 'player1', 'player2'],
  [14, 15, "Advantage player2", 'player1', 'player2'],

  [6, 4, 'Win for player1', 'player1', 'player2'],
  [4, 6, 'Win for player2', 'player1', 'player2'],
  [16, 14, 'Win for player1', 'player1', 'player2'],
  [14, 16, 'Win for player2', 'player1', 'player2'],

  [6, 4, 'Win for One', 'One', 'player2'],
  [4, 6, 'Win for Two', 'player1', 'Two'],
  [6, 5, 'Advantage One', 'One', 'player2'],
  [5, 6, 'Advantage Two', 'player1', 'Two']
]
```

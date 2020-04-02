# Easter Memory Game

## Initializing
1. There are 6 images used. There are 6 pairs of each template, making (6 x 6 = 36) cards to be flipped. These are arranged in a 6 x 6 grid.
2. Each element in the *cards* array will use a randomly determined image. A *While* loop nested within a *For* loop incrementally assigns all elements in the *cards* array till all *template* properties are no longer *undefined*.
3. *isMatched*, *isFlipping* and *isOpened* are all *false*.

## Playing
1. The *flipCard()* method is called when the user clicks on a card.
- the card's *isFlipping* property is set to *true* if *isMatched* is *false*.
- if *isOpened* is *true*, the card is closed. *isFlipping* and *isOpened* is set to *false*.
- if *isOpened* is *false*, the card is opened. *isFlipping* is set to *false* and *isOpened* is set to *true*.
  - if there is another card whose *isOpened* property is *true*, compare the two cards. If their *template* properties have the same value, they match. Set *isMatched* to true.
  - if they do not match, close both cards.
2. Whether opening or closing cards, the flipping animation is introduced to provide a slight delay so that the user can see the card images.

## Finishing
1. If *seconds* (which decrements every second) reaches 0 and there are elements in *cards* whose *isMatched* property is *false*, the game ends in failure.
2. If there are no elements in *cards* whose *isMatched* property is *false*, the game ends in success regardless of the value of *seconds*.

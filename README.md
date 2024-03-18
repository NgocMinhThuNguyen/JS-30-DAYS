# INTRO

I start this 30 vanilla JS Challenge on 18th April 2024.
This challenge is created by [Wes Bos](https://github.com/wesbos/JavaScript30).

I record what I learned and how I came up with solution in this document for future review.

# DAY 1
## Algorithm

- Get the keyCode of the keyboard's pressed character.
- Retrieve the audio element with a `data-key` attribute matching the keyCode.
- Play the audio.
- Add the class `playing` to the div element that has a `data-key` matching the keyCode.
- Wait for the animation of the `div` to finish.
- Remove the `playing` class to return the `div` to its original style.

## What I learned
- `event.keyCode`: getting the key code of the keyboard's pressed character
- `keydown` is an event fired when a key is pressed. While `keypress` event fired when a key produces a character value is pressed (`Alt`,  `Shift`, `Ctrl` are not), `keydown` listens to all keys.

# DAY 2
## Algorithm

- Transform all clock hands to 12 o'clock direction
- Get current hour, minute and second
- Calculation:
  - A clock is a circle shape that is `360deg`
  - At every hour, we rotate hour hand `30deg` plus `90deg` since we roated all clock hands to 12 o'clock direction at the beginning
  - At every minute, we rotate minute hand `6deg` plus `90deg`
  - At every second, we roate the second hand `6deg` plus  `90deg` also

## What I learned
- `Date` object provides methods that allows to get the current time

```js
const now = Date();
const hour = now.getHour();
const minute = now.getMinute();
const second = now.getSecond();
```

- `setInterval(function, delay)`: used to repeatedly execute an action or call a function after a certain period of time.

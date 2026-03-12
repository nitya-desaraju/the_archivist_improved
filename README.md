# The Archivist

The Archivist is a web-based psychological thriller game. You are a technician transferring corrupted files from an old data server to a new one. But beware. An AI anomaly lurks between. It can be played [here](https://nitya-desaraju.github.io/the_archivist_improved/).

## Introduction

I love to play video games, so I wanted to make my own! The puzzles in the game were inspired by tasks from Among Us. I also wanted to explore this genre of games, especially ones involving moral questions.

## How this works

The game is a single web-page that uses HTML, CSS, and JavaScript. There is no server-side code, making this game extremely portable.
The gameState object tracks all of the information as the player makes changes. The puzzles are randomly generated. The maze and signal puzzles are drawn on using a Canvas element. It uses browser APIs to access the player's camera and microphone.
I made the retro monitor background by using a scanline overlay, color aberration, and a flickering animation.

## Challenges

This was the most difficult project I have ever coded. I couldn't just use basic html I already knew. 
The maze puzzle was the hardest because I needed to randomly generate the maze each time using a recursive backtracking algorithm. I learned how to use Canvas to let the user draw on the maze. 
I also learned how to access external devices (camera and mic), which helped me better understand asychronous JS. I ran into a lot of problems with movement sensing, mainly because it took me a while to realize it wasn't even getting a video input in the first place. I then had to adjust how quickly it would update the level shown on the screen, because as the player moved, it would flicker too fast and glitch out. I fixed this by using a smoothing algorithm.
I had to constantly tweak puzzle timers and sensitivities after many, many rounds of testing so that the game was the right difficulty. 
I also learned to use asynchronous functions and setTimeout to prevent race conditions and add delays.
Of course, I learned a lot of styling to achieve the look that fit with the theme.

## How to play

Click on each file in the file directory and complete the puzzles to decrypt and transfer them to the secure server. However, the AI archivist might watch and listen to you as you solve a puzzle, so don't move and breathe quietly. Once you finish, decommission the server to disable the rogue AI. Make your choice...
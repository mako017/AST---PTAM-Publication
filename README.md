# Are you Swiping, or Just Marking? Development and Evaluation of the Attention Swiping Task

## Introduction

The Attention Swiping Task (AST) was developed as a computer-based test of sustained attention that can be administered on any mobile device without the need for dedicated hard- or software on the client-side.

Traditional tests of sustained attention usually require the test takers to mark targets (i.e., stimuli to which pre-learned rules apply) by either crossing them out or drawing lines beneath them. While these approaches have repeatedly been shown to result in highly reliable and valid psychological measurment instruments, they don't feel natural on mobile devices.

This repository contains the source code of the AST as it was administered by [Koch et al. (submitted)](#blank).

## Measured variables

The variables that can be exported for each participant are:

1. Response data for each item (i.e., hits, false alarms, misses, correct rejections)
2. Reaction times for each item
3. Number of mistakes during the familarization period
4. Number of repetions of the instructions

For the article by [Koch et al. (submitted)](#blank) we focused on the analysis of the data from the second category and computed the following indices described by [Moosbrugger & Oehlschlägel (2011)](#blank):

- G = total number of items attempted within the time limit
- FV = number of misses
- FA = number of false alarms
- L = attentive performance; L = G - 2 x (FV + FA)
- Q = performance quality; Q = L / G
- K = performance consistency; K = L \* Q

## Technical Details

The AST has been developed as a web app with HTML5, CSS, and JavaScript. In this version there are no external dependencies but [jQuery](https://github.com/jquery/jquery) (a local copy can be found within this repository, in case the test should be implemented for offline studies).

The AST has already been tested on a broad range of different devices and has generally worked well with few technical problems. Nonetheless, there are some noteworthy exceptions:

- E-readers are not appropriate for taking the AST as their monitor refresh rate and responsiveness is too slow
- The AST uses swiping guestures. On some devices it can happen that OS guestures override the test or lead to undesired behavior (e.g., on iOS Safari, swiping from left to right can navigate to the previous site)
- JavaScript blockers should be disabled for the AST as this can lead to unexpected behavior
- The test can also be taken on a computer with the mouse or track pad, however, it is unclear how comparable the results are because of different response speed
- In rare cases iOS devices have zoomed in on the test making it difficult to sort flowers. Double tapping usually solved the problem.

## References

Koch, M., Moeller, C., & Spinath, F.M. (submitted). _Are you Swiping, or Just Marking? Exploring the Feasibility of Psychological Testing on Mobile Devices_

Moosbrugger, H., & Oehlschlägel, J. (2011). _Frankfurter Aufmerksamkeits-Inventar 2: FAIR-2_ [Measurement instrument]. Huber.

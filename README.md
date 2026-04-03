# InteractiveElevator-web

live site: https://arpon7.github.io/InteractiveElevator-web/

SCAN Algorithm: 
The elevator uses the SCAN algorithm (also called the "Elevator Algorithm"). Here's how it works:

Core Principle
The elevator continues in its current direction (UP or DOWN) and serves all requests in that direction before reversing. This is much more efficient than going to the nearest floor each time.

Why SCAN is Better
Without SCAN (Nearest Floor First):

Current floor: 0
Requests: [3, 1, 2]
Path: 0 → 3 → 1 → 2 (travels 7 floors total)

With SCAN:

Current floor: 0, Direction: UP
Requests: [3, 1, 2]
Path: 0 → 1 → 2 → 3 (travels only 3 floors!)

The Algorithm Steps

Receive a request - Someone presses a floor button
Add to queue - If not already in the queue, add it
Sort queue based on current direction:

Going UP: Serve floors above current position first (ascending order)
Going DOWN: Serve floors below current position first (descending order)


Move to next floor in the sorted queue
Open doors → Wait 2 seconds → Close doors
Check if more requests in current direction

If yes: Continue in same direction
If no: Reverse direction and handle remaining requests


Repeat until queue is empty
Go IDLE when no requests remain

Real-World Example
Imagine you're on Floor 0 and these buttons are pressed:

Floor 2 (from inside elevator)
Floor 1 (someone calling from Floor 1)
Floor 3 (from inside elevator)

The elevator will:

Start moving UP (direction determined by first request)
Stop at Floor 1 first (lowest floor in UP direction)
Then Floor 2 (next in line)


This is an interactive web interface to simulate the working of an elevator. 
Finally Floor 3 (highest)

This prevents unnecessary back-and-forth movement!

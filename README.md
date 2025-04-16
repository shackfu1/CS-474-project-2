# Reservations

## Building

Command line:

* `make` to build. An executable called `reservations` will be produced.

## Files

* `reservations.c`: The main code to launch the project

## Data

There is one array of ints used to determine whether or not a specific seat is taken. If an index is marked 0, the seat is not taken, if it is marked as 1, it is taken.

## Functions

* `main()`
  * `seat_broker()`: A thread that randomly reserves and frees seats.
    * `verify_seat_count()`: Verifies that the seat count variable is the same as the number of seats taken.
    * `free_seat()`: Marks the seat at the specified location as free, if it isn't already.
    * `reserve_seat()`: Marks the seat at the specified location as reserved, if it isn't already.
    * `is_free()`: Checks if the seat at the specified location is free.

## Notes

* Could possibly be room to optimize performance by making the mutexes less strict.

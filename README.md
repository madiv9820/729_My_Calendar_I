# 729. My Calendar I

__Type:-__ Medium

__Topics:-__ Array, Binary Search, Design, Segment Tree, Ordered Set

__Companies:-__ Google, Flexport, Uber, Amazon, Adobe, Microsoft, Apple, Twitch

<hr>

You are implementing a program to use as your calendar. We can add a new event if adding the event will not cause a __double booking__.

A __double booking__ happens when two events have some non-empty intersection (i.e., some moment is common to both events.).<br><br>
The event can be represented as a pair of integers `start` and `end` that represents a booking on the half-open interval `[start, end)`, the range of real numbers `x` such that `start <= x < end`.<br><br>
Implement the `MyCalendar` class:
- `MyCalendar()` Initializes the calendar object.
- `boolean book(int start, int end)` Returns `true` if the event can be added to the calendar successfully without causing a __double booking__. Otherwise, return `false` and do not add the event to the calendar.

__Example 1:__<br>
    __Input:__ <br>
    ["MyCalendar", "book", "book", "book"]<br>
    [[], [10, 20], [15, 25], [20, 30]]<br>
    __Output:__ [null, true, false, true]<br>
    __Explanation__<br>
    MyCalendar myCalendar = new MyCalendar();<br>
    myCalendar.book(10, 20); // return True<br>
    myCalendar.book(15, 25); // return False, It can not be booked because time 15 is already booked by another event.<br>
    myCalendar.book(20, 30); // return True, The event can be booked, as the first event takes every time less than 20, but not including 20.<br>

__Constraints:__
- <code>0 <= start < end <= 10<sup>9</sup></code>
- At most `1000` calls will be made to `book`.
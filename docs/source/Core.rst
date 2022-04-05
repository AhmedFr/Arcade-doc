****
Core
****

General
=====
The core is the system that allows you to launch the arcade program and connect the different libraries in real time.

Keys management
=====
When the events go through the Core in order to be transmitted from the graphics library to the game library, a translation of the events is done.

All key codes are transformed to match SFML key macros according to the following codes:

Shortcuts
=====
The core can detect some shortcuts.

.. hlist::
    :columns: 1

    * **Exit:** Q
    * **Go to menu:** Escape
    * **Restart game:** R
    * **Next graphical librairy:** L
    * **Previous graphical librairy**: K
    * **Next game:** N
    * **Previous game:** B

**SFML Key codes:**

.. hlist::
    :columns: 2

    * BACKSPACE = 59
    * ENTER = 58
    * SPACE = 57
    * ESC = 36
    * LEFT_CLICK = 100
    * RIGHT_CLICK = 101
    * ARROW_UP = 73
    * ARROW_DOWN = 74
    * ARROW_LEFT = 71
    * ARROW_RIGHT = 72
    * A = 0
    * B = 1
    * C = 2
    * D = 3
    * E = 4
    * F = 5
    * G = 6
    * H = 7
    * I = 8
    * J = 9
    * K = 10
    * L = 11
    * M = 12
    * N = 13
    * O = 14
    * P = 15
    * Q = 16
    * R = 17
    * S = 18
    * T = 19
    * U = 20
    * V = 21
    * W = 22
    * X = 23
    * Y = 24
    * Z = 25

For example, here are the key codes for the SDL2 and Ncurses libraries which will be translated into SFML when passing through the Core.

**SDL2 Key codes:**

.. hlist::
    :columns: 2

    * BACKSPACE = 59
    * ENTER = 58
    * SPACE = 57
    * ESC = 36
    * LEFT_CLICK = 100
    * RIGHT_CLICK = 101
    * ARROW_UP = 73
    * ARROW_DOWN = 74
    * ARROW_LEFT = 71
    * ARROW_RIGHT = 72
    * A = 0
    * B = 1
    * C = 2
    * D = 3
    * E = 4
    * F = 5
    * G = 6
    * H = 7
    * I = 8
    * J = 9
    * K = 10
    * L = 11
    * M = 12
    * N = 13
    * O = 14
    * P = 15
    * Q = 16
    * R = 17
    * S = 18
    * T = 19
    * U = 20
    * V = 21
    * W = 22
    * X = 23
    * Y = 24
    * Z = 25

**Ncurses Key codes:**

.. hlist::
    :columns: 2

    * BACKSPACE = 59
    * ENTER = 58
    * SPACE = 57
    * ESC = 36
    * LEFT_CLICK = 100
    * RIGHT_CLICK = 101
    * ARROW_UP = 73
    * ARROW_DOWN = 74
    * ARROW_LEFT = 71
    * ARROW_RIGHT = 72
    * A = 0
    * B = 1
    * C = 2
    * D = 3
    * E = 4
    * F = 5
    * G = 6
    * H = 7
    * I = 8
    * J = 9
    * K = 10
    * L = 11
    * M = 12
    * N = 13
    * O = 14
    * P = 15
    * Q = 16
    * R = 17
    * S = 18
    * T = 19
    * U = 20
    * V = 21
    * W = 22
    * X = 23
    * Y = 24
    * Z = 25

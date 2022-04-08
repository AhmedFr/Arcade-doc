******
Events
******

Description
===========

The graphical part create event and they are used by game part.
Events are used to trigger actions in game part.
They contain key code and mouse position if event is in relation to mouse.

Interface
=========

.. code-block:: cpp

    namespace Arcade {
        struct Pos {
            int x;
            int y;
        };
        class IEvent {
            public:
                virtual ~IEvent() = default;

                virtual std::size_t getKey() const = 0;   // Get key
                virtual void setKey(std::size_t const key) = 0;   // Set key
                virtual Pos getMousePos() const = 0;  // Get mouse pos
                virtual std::string getData() const = 0;    // Get event text data
        };
    }

- **getKey:** Get key code, code are based on the SFML key code, see "Key Macro" below
- **getMousePos:** Get mouse position, when event isn't a mouse event return a Pos(0, 0)
- **getData:** Get text data

.. note:: The text data is notably used for players names or libs names in assocation with the **IGame::sendEvent** fonction.

Key Code
========

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
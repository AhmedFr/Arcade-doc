*****
Games
*****

Description
===========

To have some fun with our arcade having games to play would be great.

Sadly our arcade can't run every game that exists, but we can promise you one thing:

If your game has been developed with the **IGame** interface it will 100% run on our Arcade!

.. note::
    The game is composed of two partts, the game logic / the actual game, and the part that says what should be 
    displayed where and how so the display libs can display the game. The scond part is done by using the IComponent interface.

.. warning:: 
    The component list that the games have should be in the order in which you want to display your stuff.
    ex: the background component is in the first position of the list and the player component must be placed further away in the list.

Interface
=========

.. code-block:: cpp

    namespace Arcade {
        class IGame {
            public:
                virtual ~IGame() = default;

                virtual void init() = 0;
                virtual void stop() = 0;
                virtual std::string getGameName() const = 0;
                virtual std::vector<std::unique_ptr<IComponent>> &getComponents() = 0;
                virtual void sendEvents(std::vector<std::unique_ptr<IEvent>> &events) = 0;
                virtual IEvent *getEvent() = 0;
                virtual void sendDisplayLibs(std::vector<std::string> const libs) = 0;
                virtual void sendGameLibs(std::vector<std::string> const libs) = 0;
                virtual void setPlayerName(std::string const name) = 0;
                virtual std::string getPlayerName() const = 0;
        };
    }

All these functions are here to make sure that the core and the game are able to send each other the needed information

.. hlist::
    :columns: 1

    * Init: Called when the game is launched
    * Stop: Called when the game is closed
    * getGameName: Return the name of the game
    * getComponents: Return components to the graphical parts
    * sendEvents: Send events to process to the game
    * getEvent: Retrieve an event from the game, for example a library change order.
    * sendDisplayLibs: Send a list of graphics libraries.
    * sendGameLibs: Send a list of graphics libraries.
    * setPlayerName: Set the name of the current player
    * getPlayerName: Return the name of the current player

Take a look at how we handle the :ref:`Scores:Scores` in our games.


And here are some of the games we made :ref:`SolarFox:SolarFox`, :ref:`Nibbler:Nibbler` & :ref:`Menu:Menu`.
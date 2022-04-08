*****
Games
*****

Description
===========

To have some fun with our arcade having games to play would be great.

Sadly our arcade can't run every game that exists, but we can promise you one thing:

If your game has been developed with the **IGame** interface it will 100% run on our Arcade!


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

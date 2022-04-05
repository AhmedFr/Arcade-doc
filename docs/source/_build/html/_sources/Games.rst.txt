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

Init & Stop functions are used by the core to initiate the game and stop it when needed.

Then the core will in a loop call the getComponents function and sendEvents function while the game is running.
The first one is to get the components from the game to then give the to the Display lib.
And in return the core gives to the game the events that happened by calling the sendEvents function.
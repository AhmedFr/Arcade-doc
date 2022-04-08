********
Displays
********

Description
===========

Display part deals with components to display them.
This part also take care of get event to send them to the game part.


Interface
=========

.. code-block:: cpp

    namespace Arcade {
        class IDisplay {
            public:
                virtual ~IDisplay() = default;

                virtual void init() = 0;
                virtual void stop() = 0;
                virtual std::string getLibName() const = 0;
                virtual void display(std::vector<std::unique_ptr<IComponent>> &components) = 0; // Display with components
                virtual std::vector<std::unique_ptr<IEvent>> &getEvents() = 0;
        };
    }

All these functions are here to make sure that the core and the display are able to send each other the needed information

- **init:** Called when the display is launched
- **stop:** Called when the display is closed
- **getLibName:** Return the name of the lib
- **display:** Display components from the game parts
- **getEvents:** Return the new events

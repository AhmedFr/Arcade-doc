************
Displays
************
Welcome to the Displays Doc !
===================================

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
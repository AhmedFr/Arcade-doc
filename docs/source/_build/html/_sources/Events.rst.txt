************
Events
************
Welcome to the Events Doc !
===================================

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
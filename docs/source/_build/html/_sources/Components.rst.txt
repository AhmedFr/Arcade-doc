************
Components
************
Welcome to the Components Doc !
===================================

.. code-block:: cpp

    #include <string>

    namespace Arcade {
        struct Rect {
            int x;
            int y;
            int width;
            int height;
        };
        class IComponent {
            public:
                enum Type {
                    OBJECT,
                    SOUND,
                    TEXT
                };
                virtual ~IComponent() = default;

                virtual std::size_t getId() const = 0;   // Get component ID
                virtual Type getType() const = 0;   // Get component type
                virtual std::string getFile() const = 0;    // Get file associated with component
                virtual int getX() const = 0;   // Get X position (OBJECT/TEXT)
                virtual int getY() const = 0;   // Get Y position (OBJECT/TEXT)
                virtual int getWidth() const = 0;   // Get width (OBJECT/TEXT)
                virtual int getHeight() const = 0;   // Get height (OBJECT/TEXT)
                virtual int getFontSize() const = 0;    // Get text (TEXT)
                virtual Rect getRect() const = 0;   // Get animated sprite rect (OBJECT) #THROW if no rect
                virtual std::string getText() const = 0;    // Get font size (TEXT)

                virtual void setX(std::size_t const x) = 0;
                virtual void setY(std::size_t const y) = 0;
                virtual void setText(std::string const text) = 0;
        };
    }
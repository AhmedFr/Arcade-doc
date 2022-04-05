**********
Components
**********

Description
===========

Component contain information to describe object drawn by display part.
There are 3 component type from Type enum: OBJECT, TEXT and SOUND.
It's possible to select drawn area thanks to Rect data, this gives us the opportunity to animate component with sprite sheet for example.

.. warning::
   Components are displayed in order of the vector not in order of id

Interface
=========

.. code-block:: cpp

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

                virtual std::size_t getId() const = 0;
                virtual Type getType() const = 0;
                virtual std::string getFile() const = 0;
                virtual int getX() const = 0;
                virtual int getY() const = 0;
                virtual int getWidth() const = 0;
                virtual int getHeight() const = 0;
                virtual int getFontSize() const = 0;
                virtual Rect getRect() const = 0;
                virtual std::string getText() const = 0;

                virtual void setX(std::size_t const x) = 0;
                virtual void setY(std::size_t const y) = 0;
                virtual void setText(std::string const text) = 0;
                virtual void setRect(Rect const rect) = 0;
        };
    }

- **getId:** Return component id
- **getType**: Return component type (OBJECT, SOUND, TEXT)
- **getFile**: Return file path => OBJECT or SOUND
- **getX**: Return x position (in percent)
- **getY**: Return y position (in percent)
- **getWidth**: Return width (in percent)
- **getHeight**: Return height (in percent)
- **getFontSize**: Return font size => TEXT
- **getRect**: Return Rect (in pixels) => OBJECT or SOUND
- **getText**: Return string => TEXT
- **setX**: Set x position (in percent)
- **setY**: Set y position (in percent)
- **setText**: Set string => TEXT
- **setRect**: Set Rect (in pixels) => OBJECT or SOUND
**********
Components
**********

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

.. hlist::
    :columns: 1

    * getId:
    * getType:
    * getFile:
    * getX:
    * getY:
    * getWidth:
    * getHeight:
    * getFontSize:
    * getRect:
    * getText:
    * setX:
    * setY:
    * setText:
    * setRect:

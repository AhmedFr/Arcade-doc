This is how you have a big header
===================================

This is how you have a normal header
------------------------------------

``Un petit bout de code``

Un gros bout de code:

.. code-block:: cpp

   namespace Arcade {
      class IDisplay {
         public:
            virtual ~IDisplay() = default;
            virtual void init() = 0;
            virtual void stop() = 0;
            virtual std::string getLibName() const = 0;
            virtual void display(std::vector<std::unique_ptr<IComponent>> &components) = 0; // Display with components
            virtual void clear() = 0; // Clear display
            virtual std::vector<std::unique_ptr<IEvent>> &getEvents() = 0;
      };
   }

Pour avoir une réference à du texte il faut un tiret du bas '_' à la fin du texte répeter
ex: Contents_

Pour faire une liste Utiliser ``-`` :

- element
- element

   Pour avoir une citation il suffit d'un tab

>>> print "On peut carrément avoir du python, une dinguerie"

Pour faire un tableau ta3 les BOGOSS
====================================

+------------+------------+-----------+
| Header 1   | Header 2   | Header 3  |
+============+============+===========+
| body row 1 | column 2   | column 3  |
+------------+------------+-----------+
| body row 2 | Cells may span columns.|
+------------+------------+-----------+
| body row 3 | Cells may  | - Cells   |
+------------+ span rows. | - contain |
| body row 4 |            | - blocks. |
+------------+------------+-----------+


Ici pour voir comment rajouter une image
====================================
.. image:: ImagePepe.png

.. note::
   This is the Syntax to create a note box

.. warning:: 
   This is the Syntax to create a warning box

Ici on peut mettre des petits trucs comme ca pour spécifier le nom d'une variable

.. cpp:class:: 
   IDisplay

.. cpp:enum::
   UNDEFINED
   TRUE 
   FALSE

Contents
--------

.. toctree::

   usage
   api

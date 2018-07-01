Lists
=====
       
Nested lists
------------

A nested list is a list that appears as an element in another list. In this
list, the element with index 3 is a nested list:

    .. code-block:: python
        
        >>> nested = ["hello", 2.0, 5, [10, 20]]

If we output the element at index 3, we get:

    .. code-block:: python

       >>> print(nested[3]) 
       [10, 20]

To extract an element from the nested list, we can proceed in two steps:

    .. code-block:: python
        
        >>> elem = nested[3]
        >>> elem[0]
        10

Or we can combine them:

    .. code-block:: python
        
        >>> nested[3][1]
        20

Bracket operators evaluate from left to right, so this expression gets the
3'th element of ``nested`` and extracts the 1'th element from it.

Matrices
--------

Nested lists are often used to represent matrices. For example, the matrix:

    .. code-block:: python
        
        >>> mx = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]

``mx`` is a list with three elements, where each element is a row of the
matrix. We can select an entire row from the matrix in the usual way:

    .. code-block:: python
        
        >>> mx[1]
        [4, 5, 6]

Or we can extract a single element from the matrix using the double-index form:

    .. code-block:: python
        
        >>> mx[1][2]
        6

The first index selects the row, and the second index selects the column.
Although this way of representing matrices is common, it is not the only
possibility. A small variation is to use a list of columns instead of a list of
rows. Later we will see a more radical alternative using a dictionary.

Glossary
--------

    aliases
        Multiple variables that contain references to the same object.

    clone
        To create a new object that has the same value as an existing object.
        Copying a reference to an object creates an alias but doesn't clone the
        object.

    delimiter
        A character or string used to indicate where a string should be split.

    element
        One of the values in a list (or other sequence). The bracket operator
        selects elements of a list.  Also called *item*.

    immutable data value
        A data value which cannot be modified.  Assignments to elements or
        slices (sub-parts) of immutable values cause a runtime error.

    index
        An integer value that indicates the position of an item in a list.
        Indexes start from 0. 
        
    item
        See *element*.

    list
        A collection of values, each in a fixed position within the list.
        Like other types ``str``, ``int``, ``float``, etc. there is also a
        ``list`` type-converter function that tries to turn whatever argument 
        you give it into a list. 

    list traversal
        The sequential accessing of each element in a list.

    modifier
        A function which changes its arguments inside the function body. Only
        mutable types can be changed by modifiers.
        
    mutable data value
        A data value which can be modified. The types of all mutable values 
        are compound types.  Lists and dictionaries are mutable; strings
        and tuples are not.

    nested list
        A list that is an element of another list.

    object
        A thing to which a variable can refer.
        
    pattern
        A sequence of statements, or a style of coding something that has
        general applicability in a number of different situations.  Part of
        becoming a mature Computer Scientist is to learn and establish the
        patterns and algorithms that form your toolkit.  Patterns often 
        correspond to your "mental chunking".   

    promise
        An object that promises to do some work or deliver some values if
        they're eventually needed, but it lazily puts off doing the work immediately.
        Calling ``range`` produces a promise.         

    pure function
        A function which has no side effects. Pure functions only make changes
        to the calling program through their return values.

    sequence
        Any of the data types that consist of an ordered collection of elements, with
        each element identified by an index.
        
    side effect
        A change in the state of a program made by calling a function. Side
        effects can only be produced by modifiers.

    step size
        The interval between successive elements of a linear sequence. The
        third (and optional argument) to the ``range`` function is called the
        step size.  If not specified, it defaults to 1.


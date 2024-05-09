Revisión y Versiones
=====

.. _installation:

+----------------------------+-------------------+--------------------+--------------+
|Nombres y Apellidos         | Versión Aprobada |  Cargo              |   Fecha      |
+============================+==================+=====================+==============+
| Marco Antonio González     |       1.0        |Desarrollador Junior
+--------------+-------------+------------------|---------------------|--------------|
| José Manuel Pájaro         |       1.0        |Desarrollador Junior
+--------------+-------------+------------------|---------------------|--------------|
| Omar Moreno                |       1.0        |Líder Técnico
+--------------+-------------+------------------|---------------------|--------------|


====


.. code-block:: console

   (.venv) $ pip install lumache

Creating recipes
----------------

To retrieve a list of random ingredients,
you can use the ``lumache.get_random_ingredients()`` function:

.. autofunction:: lumache.get_random_ingredients

The ``kind`` parameter should be either ``"meat"``, ``"fish"``,
or ``"veggies"``. Otherwise, :py:func:`lumache.get_random_ingredients`
will raise an exception.

.. autoexception:: lumache.InvalidKindError

For example:

>>> import lumache
>>> lumache.get_random_ingredients()
['shells', 'gorgonzola', 'parsley']


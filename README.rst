Kylin DBAPI Driver and Sqlalchemy Dialect
==============================

Installation
------------

To install this driver run::

    $ pip install pykylin

or from source::

    $ pip install -r ./requirements.txt
    $ python setup.py install


Usage
-----
.. code-block:: python

    import pykylin
    query_text = "SELECT dt, SUM(users) FROM table GROUP BY dt"
    cursor = pykylin.connect(username='username',password='password',
                             endpoint='http://yourkylinadress/kylin/api',
                             project='project_name').cursor()
    cursor.execute(query_text)
    print cursor.fetchall()
    cursor.close()

More info
---------

 * http://kylin.incubator.apache.org/
 * http://www.sqlalchemy.org/


Authors
-------

 * Wu Xiang

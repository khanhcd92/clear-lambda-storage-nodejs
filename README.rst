Clear Lambda code storage
===========================


Motivation
-----------
AWS limits the total code storage for Lambda functions to `75GB <https://docs.aws.amazon.com/lambda/latest/dg/limits.html#limits-list>`_.

The main reason of reaching such size is because for every deployment of existing function, AWS stores the previous version ("qualifier").

Usually, when you reach that point, you want to remove old version.
This tool will help you to!


Setup
-----
Install via source

.. code-block:: bash

    git clone https://github.com/khanhcd92/clear-lambda-storage-nodejs.git
    cd clear-lambda-storage-nodejs/
    npm i
    node index.js


Advanced usage
---------------

Provide credentials:

.. code-block:: bash

    node index.js --token-key-id <access_key_id> --token-secret <secret_access_key>

Provide credentials with specific region:

.. code-block:: bash

    node index.js --token-key-id <access_key_id> --token-secret <secret_access_key>

Alternate usage:
.. code-block:: bash

    node index.js --profile-id <profile_id> --num-to-keep 2
=========
New Relic
=========

If you are using NewRelic, you will want to use the hooks provided, otherwise
all Nap API calls will be logged as "nap.rest.publisher.view".

Simply add the following lines to your newrelic.ini

.. code-block:: ini

    [import-hook:nap.rest.publisher]
    enabled = true
    execute = nap.newrelic:instrument_django_nap_publisher

    [import-hook:nap.rpc.RPCView]
    enabled = true
    execute = nap.newrelic:instrument_django_nap_publisher

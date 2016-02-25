rabbitmq_server Docs
====================

Install clustered RabbitMQ


Basic Role Example
^^^^^^^^^^^^^^^^^^

.. code-block:: yaml

    - name: Install rabbitmq server
      hosts: rabbitmq_all
      max_fail_percentage: 20
      user: root
      roles:
        - { role: "rabbitmq_server", tags: [ "rabbitmq-server" ] }
      vars:
        rabbitmq_cookie_token: secrete
        container_address: "{{ ansible_ssh_host }}"


Role overrides
^^^^^^^^^^^^^^

rabbitmq_async_threads
  This override defaults to 128 threads for IO operations inside the erlang VM

rabbitmq_process_limit
  This override defaults to 1048576 for number of concurrent processes inside the erlang VM
  Each network connection and file handle does need its own process inside erlang

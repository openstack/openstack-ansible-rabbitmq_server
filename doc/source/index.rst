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

OpenStack-Ansible RabbitMQ Server
#################################

This Ansible role deploys RabbitMQ. When multiple hosts are present in the
rabbitmq_all inventory group a cluster will be created.

Default Variables
=================

.. literalinclude:: ../../defaults/main.yml
   :language: yaml
   :start-after: under the License.

Required Variables
==================

.. code-block:: yaml

    # RabbitMQ cluster shared secret
    rabbitmq_cookie_token: secrete

Example Playbook
================

.. code-block:: yaml

    - name: Install rabbitmq server
      hosts: rabbitmq_all
      user: root
      roles:
        - { role: "rabbitmq_server", tags: [ "rabbitmq-server" ] }
      vars:
        rabbitmq_cookie_token: secrete


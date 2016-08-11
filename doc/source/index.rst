=================================
OpenStack-Ansible RabbitMQ server
=================================

This Ansible role deploys RabbitMQ. When multiple hosts are present in
the ``rabbitmq_all`` inventory group, a cluster is created.

Table of Contents
~~~~~~~~~~~~~~~~~

.. toctree::
   :maxdepth: 2

   configure-rabbitmq.rst


Default variables
~~~~~~~~~~~~~~~~~

.. literalinclude:: ../../defaults/main.yml
   :language: yaml
   :start-after: under the License.

Required variables
~~~~~~~~~~~~~~~~~~

.. code-block:: yaml

    # RabbitMQ cluster shared secret
    rabbitmq_cookie_token: secrete

Example playbook
~~~~~~~~~~~~~~~~

.. literalinclude:: ../../examples/playbook.yml
   :language: yaml

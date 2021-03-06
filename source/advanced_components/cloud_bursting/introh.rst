.. _introh:

================================================================================
Overview
================================================================================

Cloud bursting is a model in which the local resources of a Private Cloud are combined with resources from remote Cloud providers. The remote provider could be a commercial Cloud service, such as Amazon EC2 or Microsoft Azure. Such support for cloud bursting enables highly scalable hosting environments.

|image0|

OpenNebula’s approach to cloud bursting is based on the transparency to both end users and cloud administrators to use and maintain the cloud bursting functionality. The **transparency to cloud administrators** comes from the fact that a AWS EC2 region or an Azure location is modeled as any other host (albeit of potentially a much bigger capacity), so the scheduler can place VMs in the external cloud as it will do in any other local host.

On the other hand, the **transparency to end users** is offered through the hybrid template functionality: the same VM template in OpenNebula can describe the VM if it is deployed locally and also if it gets deployed in EC2, or Azure. Therefore users just have to instantiate the template, and OpenNebula will transparently choose if that is executed locally or remotely.

How Should I Read This Chapter
================================================================================

You should be reading this Chapter as part of the :ref:`Advanced Components Guide <advanced_components>` review of that OpenNebula advanced functionality that you are interested in enabling and configuring.

Within this Chapter you can find a guide to configure and use the :ref:`Amazon EC2 driver <ec2g>` and the :ref:`Azure driver <azg>`. Additionally, there is support of IBM SoftLayer available as add-on (ie, not contained in the OpenNebula main distribution) `here <https://github.com/OpenNebula/addon-softlayer>`__.

Once the cloud architecture has been designed the next step would be to learn how to install the :ref:`OpenNebula front-end <opennebula_installation>`.

Hypervisor Compatibility
================================================================================

All the Sections in this Chapter applies to both KVM and vCentre based OpenNebula clouds.

.. |image0| image:: /images/hybridcloud.png

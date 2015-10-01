# Playa Mesos x4

Playa Mesos helps you quickly create [Apache Mesos](http://mesos.apache.org/)
test environments.  A VirtualBox image, which has Mesos, Marathon, and Chronos
is built from source using Packer.

## Requirements

* [VirtualBox](http://www.virtualbox.org/) 4.2+
* [Vagrant](http://www.vagrantup.com/) 1.3+
* [Packer](http://www.packer.io) 0.5+
* [git](http://git-scm.com/downloads)

## Quick Start

1. [Install VirtualBox](https://www.virtualbox.org/wiki/Downloads)
2. [Install Vagrant](http://www.vagrantup.com/downloads.html)
3. [Install Packer](https://www.packer.io/downloads.html)

4. Update your PATH to point to Packer.
  ```bash
  export PATH=$PATH:/path/where/i/extracted/packer/archive/
  ```

5. Clone this repository
  ```bash
  git clone https://github.com/kaysoky/playa-mesos.git
  cd playa-mesos
  ```

6. Make sure tests pass
  ```bash
  bin/test
  ```

7. Destroy any existing VM
  ```bash
  vagrant destroy
  ```

8. Build the Vagrant box image
  ```bash
  bin/build
  ```

9. Start the VM
  ```bash
  vagrant up
  ```

10. Do stuff
  Mesos Web UI: [10.141.141.10:5050](http://10.141.141.10:5050)

  Marathon Web UI: [10.141.141.10:8080](http://10.141.141.10:8080)

  SSH to the VM
    ```bash
    vagrant ssh
    ...
    exit
    ```

11. Halt the VM
  ```bash
  vagrant halt
  ```

12. Destroy the VM
  ```bash
  vagrant destroy
  ```

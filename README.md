# Ansible Role: Java

Installs Java for RedHat/CentOS and Debian/Ubuntu linux servers.

## Role Variables

Available variables are listed below, along with default values:

    # The defaults provided by this role are specific to each distribution.
    java_packages:
      - java-1.7.0-openjdk

Set the version/development kit of Java to install, along with any other necessary Java packages.
## Example Playbook (using default package, usually OpenJDK 7)

    - hosts: servers
      roles:
        - Javarole

## Example Playbook (install OpenJDK 8)

For RHEL / CentOS:

    - hosts: server
      roles:
        - role: Javarole
          when: "ansible_os_family == 'RedHat'"
          java_packages:
            - java-1.8.0-openjdk



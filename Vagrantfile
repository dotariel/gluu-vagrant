# -*- mode: ruby -*-
# vi: set ft=ruby :

# The hostname and IP mapping must exist in 
# /etc/hosts
ip = "192.168.2.120"
hostname = "gluu.local"

Vagrant.configure("2") do |config|
    config.vm.box = "centos/7"
    config.vm.network "private_network", ip: ip
    config.vm.hostname = hostname

    config.vm.provision :ansible do |ansible|
      ansible.playbook = "ansible/site.yml"
      ansible.extra_vars = {
        server_ip: ip,
        server_hostname: hostname,
        ldap_pass: "admin123",
        cert_org_name: "ACME",
        cert_country_code: "US",
        cert_city: "Beverly Hills",
        cert_state: "CA"
      }
    end

    config.vm.synced_folder ".", "/vagrant", :mount_options => ["dmode=777", "fmode=666"]
end



Vagrant.configure("2") do |config|

  config.vm.define :galaxy1 do | galaxy1 |

    galaxy1.vm.box = "ubuntu/jammy64"
    galaxy1.vm.network  :private_network, ip: "192.168.56.13"
    galaxy1.vm.host_name = "galaxy1"

    galaxy1.vm.provision :ansible do | ansible |
      ansible.galaxy_role_file = "galaxy1/requirements.yml"
      ansible.inventory_path = "./galaxy1/galaxyservers.inv"
      ansible.playbook = "./galaxy1/main.yml"
      ansible.host_key_checking = false
      ansible.limit='all'
    end

  end

end



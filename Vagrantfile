# Vagrantfile para configurar uma VM Ubuntu 20.04
Vagrant.configure("2") do |config|
   
# Define a box oficial do Ubuntu 20.04
  config.vm.box = "ubuntu/focal64"

# Define porta de acesso no host 8090 e habilita ip externo
  config.vm.network "forwarded_port", guest: 80, host: 8090
  config.vm.network "public_network", ip: "192.168.100.55"

# Define o nome da máquina virtual
  config.vm.define "vm--nginx-vm" do |vm|
  vm.vm.hostname = "vm--nginx-vm"
   
# Configuração de provisionamento via Shell Script
  vm.vm.provision "shell", path: "provision.sh"

# Configuração de sincronização de pastas
  vm.vm.synced_folder "site", "/var/www/html"
  
# Configuração de recursos
  vm.vm.provider "virtualbox" do |vb|
    vb.memory = "1024" # Memória RAM de 1 GB
    vb.cpus = 1        # 1 núcleo de CPU

    end
  end
end
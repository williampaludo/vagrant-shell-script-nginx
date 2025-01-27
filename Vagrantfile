# Vagrantfile para configurar uma VM Ubuntu 20.04
Vagrant.configure("2") do |config|
    # Define a box oficial do Ubuntu 20.04
    config.vm.box = "ubuntu/focal64"
  
    # Define o nome da máquina virtual
    config.vm.define "vm--nginx-vm" do |vm|
      vm.vm.hostname = "vm--nginx-vm"
  
      # Configuração de sincronização de pastas
      vm.vm.synced_folder "./site", "/var/www/html"
  
      # Configuração de provisionamento via Shell Script
      vm.vm.provision "shell", path: "provision.sh"
  
      # Configuração de recursos
      vm.vm.provider "virtualbox" do |vb|
        vb.memory = "1024" # Memória RAM de 1 GB
        vb.cpus = 1        # 1 núcleo de CPU
      end
    end
  end
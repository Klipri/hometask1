Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"

  config.vm.network "forwarded_port", guest: 80, host: 8888

  config.vm.provision "shell", inline: <<-SHELL
    yum install -y epel-release
    yum install -y nginx
    systemctl start nginx
    systemctl enable nginx
  SHELL 
#Shell - оболонка, команди, які виконуються при запуску Virtual Machine

config.vm.synced_folder "C:/Users/Legion/Desktop/hometask1/www-content", "/usr/share/nginx/html"

end
Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"
  config.vm.hostname = "master"
  config.vm.network "private_network", ip: "192.168.50.10"
  config.vm.synced_folder  "src/", "/var/www/html"
  config.vm.provision "shell", inline: <<-samplescript  
  yum install -y httpd
  systemctl enable httpd
  systemctl start httpd
  samplescript
  config.vm.provider "vitualbox" do |vb|
   vb.memory = "1024"
   vb.cpu = "2"
  end   
end

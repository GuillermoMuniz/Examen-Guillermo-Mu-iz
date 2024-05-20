
Vagrant.configure("2") do |config|
 
  config.vm.box = "ubuntu/xenial64"
  config.vm.network "private_network", ip: "192.168.50.55"
  
  config.vm.synced_folder ".", "/Examen-Tema7-Guillermo"



  config.vm.provision "shell", inline: <<-SHELL
  
  
      
   sudo apt install -y nginx
   sudo apt-get update
   
  
 
echo "-- Insertar datos de ejemplo en la tabla 'platos'" > /home/vagrant/datos_menu.sql
echo "INSERT INTO datos_menu.platos (platoID, platoNombre, precioPlato ) VALUES" >> /home/vagrant/datos_menu.sql
echo "(1, 'Ensalada', 5)," >> /home/vagrant/datos_menu.sql
echo "(2, 'Escalopines', 10)," >> /home/vagrant/datos_menu.sql
echo "(3, 'Lubina', 10)," >> /home/vagrant/datos_menu.sql
echo "(4, 'Helado', 3)" >> /home/vagrant/datos_menu.sql



SHELL

end


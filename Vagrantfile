
Vagrant.configure("2") do |config|
 
  config.vm.box = "ubuntu/xenial64"
  config.vm.network "private_network", ip: "192.168.50.55"
  
  config.vm.synced_folder ".", "/Examen-Tema7-Guillermo"



  config.vm.provision "shell", inline: <<-SHELL
  
  
   sudo apt install mysql-server  
   sudo apt install -y nginx
   sudo apt-get update
   
  
 
echo "-- Insertar datos de ejemplo en la tabla 'menu'" > /home/vagrant/gestion_restaurante.sql
echo "INSERT INTO gestion_restaurante.menu (IDplato, nombre, descripcion, precio, categoria ) VALUES" >> /home/vagrant/gestion_restaurante.sql
echo "(1, 'Ensalada', 'Ensalada con pollo', 5, 'entrante')," >> /home/vagrant/gestion_restaurante.sql
echo "(2, 'Escalopines', 'Escalopines al cabrales', 10, 'segundo')," >> /home/vagrant/gestion_restaurante.sql
echo "(3, 'Lubina', 'Lubina al horno', 10, 'segunda opcion')," >> /home/vagrant/gestion_restaurante.sql
echo "(4, 'Helado', 'Bombon de la ibense', 2, 'postre');" >> /home/vagrant/gestion_restaurante.sql



SHELL

end


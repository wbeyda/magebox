install php7.1 from ppa
install apache2 from ppa
sudo apt-get install php7.3-xml
sudo apt-get install php7.3-soap

enable php7.3-soap in /etc/php/7.3/cli/php.ini
find which PHP apache is using: 
    php -i | grep "php.ini"
increase memory_limit=2048 in /etc/php/7.3/apache2/php.ini

provision and reload vagrant with more memory
Vagrant.configure("2") do |config|
    # usual vagrant config here

    config.vm.provider "virtualbox" do |v|
        v.memory = 4096
        v.cpus = 4
    end
end

admin url: admin_safe
table prefix: mg_

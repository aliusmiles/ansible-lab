Vagrant.configure('2') do |config|
  config.vm.box = 'ubuntu/xenial64'
  config.vm.hostname = 'ansible-lab'
  config.vm.box_check_update = false
  config.vm.provider 'virtualbox' do |vb|
    # remove ubuntu log file
    vb.customize ['modifyvm', :id, '--uartmode1', 'disconnected']
  end
  config.vm.synced_folder '.', '/vagrant', disabled: true
  config.vm.provision 'shell', inline: 'apt update && apt install python-pip -y && pip install -U ansible awscli'
end

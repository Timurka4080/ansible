# Инструкции
Для проверки надо скачать репозиторий 

	cd ~
    git clone git@github.com:Timurka4080/ansible.git
	
После этого зайдите в директорию ansible и запускаем виртуальные машины с помощью vagrant

	cd ~/ansible/
	vagrant up 

Для подключения к хосту nginx нам необходимо будет передать множество
параметров - это особенность Vagrant. Узнать эти параметры можно с
помощью команды vagrant ssh-config.    

Далее можно запустить простой playbook командой 

    ansible-playbook provision/playbook.yml

Или можно запустить playbook в role    

    ansible-playbook -vv nginx-role/tasks/main.yml
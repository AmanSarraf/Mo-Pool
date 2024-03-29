WORK IN PROGRESS!
USE AT YOUR OWN RISK!

# MO Pool

Deploy a MineOnlium pool in a few simple steps :) 

## System Requirements
* Fast (150+mbs) and stable internet connection 
* SSD (recomended)
* memory >= 8gb  (If you take the block explorer out you might be able to get down to 4gb)
* cpu >= 4 ( Once again if you strip some services out you can probably cut this back)


## Services Rendered:
* [Grafana](https://grafana.com/): 3001
* BlockExplorer: 40001
* Stratum Mining Server: 4073
* Mining Server Frontend: 3000


# Get started
## English / ENG
1. If you are on windows, install WSL2 - https://ubuntu.com/tutorials/install-ubuntu-on-wsl2-on-windows-10#1-overview. Linux and OSX do not need this.
1. Docker (or docker desktop if you have GUI) - https://docs.docker.com/engine/install/ubuntu/#install-using-the-convenience-script
1. download https://github.com/MineOnliumOfficial/Mo-Pool/archive/refs/heads/main.zip - repo.
1. extract repo
1. go to the repository folder
1. edit .env (this file is hidden, search for how to view hidden files in your system)
1. edit miningcore.js ( located at `MO-Stack/Miningcore.UI-master/be/cmd/be/kodata/js/miningcore.js`)
1.you move to the address bar of the browser (while you are in the repository folder) and enter "cmd" - enter the command `Docker compose up -d`
1. Learn how to monitor and view logs of the running containers here -> https://docs.docker.com/engine/reference/commandline/container_ls/
1. After the node has reached synchronization. Enter the command `docker compose -f docker-compose.mc.yml up -d` to bring up the Miningcore stack. 
1. Then you also open another terminal and enter the command `docker compose -f docker-compose.bs.yml up -d` to bring up the Block Explorer.
1. Open port 4073 and 60606 in Ubuntu. to do this, open the Ubuntu terminal via start. enter the command "sudo ufw allow 4073" and  "sudo ufw allow 60606"

## Russian / RU

Установка собственного пула в локальной сети
1. Если вы используете Windows, установите WSL2 - https://ubuntu.com/tutorials/install-ubuntu-on-wsl2-on-windows-10#1-overview . Если у вас Linux и OSX пропускайте этот пункт.
1.  Docker (или рабочий стол docker, если у вас есть графический интерфейс) - https://docs.docker.com/engine/install/ubuntu/#install-using-the-convenience-script
1. Скачайте репозиторий https://github.com/MineOnliumOfficial/Mo-Pool/archive/refs/heads/main.zip
1. Распакуйте репозиторий в нужную папку.
1. Перейдите в папку репозитория
1. Отредактируйте .env (этот файл можно изменить с помощью блокнота, файл возможно скрыт, найдите, как просмотреть скрытые файлы в вашей системе)
1. Отредактируйте miningcore.js ( ..папка репозитория\Miningcore.UI-master\be\cmd\be\kodata\js)
1. Перейдите в адресную строку эксплорера (пока находитесь в папке репозитория) и вводите "cmd" , в открывшемся терминале вводите команду: "Docker compose up -d"
1. Посмотрите, как отслеживать и просматривать журналы запущенных контейнеров, здесь -> https://docs.docker.com/engine/reference/commandline/container_ls/
1. После того, как узел достигнет синхронизации, введите следующую команду "docker compose -f docker-compose.mc.yml up -d", чтобы вызвать стек Miningcore.
1. Затем таким же способом открывайте другой терминал в этой же папке и вводите команду "docker compose -f docker-compose.bs.yml up -d", чтобы вызвать проводник блоков.
1. Теперь вам нужно открыть порты 4073 и 60606 в Ubuntu. Чтобы сделать это, откройте терминал Ubuntu через пуск. Введите команды "sudo ufw разрешить 4073" и "sudo ufw разрешить 60606".
1. Стратум вашего майнинг пула в локальной сети будет – локальный ip:4073
Готово!

## Chineese / zh-CHT

1. 如果你是在windows上，请安装WSL2
https://ubuntu.com/tutorials/install-ubuntu-on-wsl2-on-windows-10
#overview。Linux和OSX不需要这个。
2. Docker（或docker桌面，如果你有GUI的话） - https://docs.docker.com/engine/install/ubuntu/#install-using-the-convenience-script
3. 下载https://github.com/MineOnliumOfficial/Mo-Pool/archive/refs/heads/main.zip 
3-1.解压 repo
3-2.进入repo的文件夹
3-3. 编辑.env（这个文件是隐藏的，搜索如何查看系统中的隐藏文件）。
3-4.编辑Miningcore.js（位于MO-Stack/Miningcore.UI-master/be/cmd/be/kodata/js/miningcore.js)
3-5.你移动到浏览器的地址栏（当你在版本库文件夹中时），输入 "cmd" - 输入命令 "Docker compose up -d"
3-6. 在这里了解如何监控和查看运行中的容器的日志-->https://docs.docker.com/engine/reference/commandline/container_ls/
3-7. 节点达到同步后。输入命令 "docker compose -f docker-compose.mc.yml up -d "来调出Miningcore栈。
3-8.然后你也打开另一个终端，输入命令 "docker compose -f docker-compose.bs.yml up -d "来调出Block Explorer。
现在你需要在Ubuntu中打开4073和60606端口。要做到这一点，通过启动打开Ubuntu终端，输入命令 "sudo ufw allow 4073" 和 "sudo ufw allow 60606"

( dont forget to open port 60606 for p2p networking :) ) 

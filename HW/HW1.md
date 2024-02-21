Развернуть две виртуальные машины (кто еще не сделал, можно последовательно)
- Ubuntu
- Centos

Затем:
Ubuntu
1. Произвести минимальную настройку (время, локаль, custom motd)
   
  a)Data

![screen](https://github.com/Flyn88/PNG/blob/main/Data.png)

  b) local  
  
![screen](https://github.com/Flyn88/PNG/blob/main/local.png)
![screen](https://github.com/Flyn88/PNG/blob/main/local%20update.png)
![screen](https://github.com/Flyn88/PNG/blob/main/local_update.png)

  c) motd
  
![screen](https://github.com/Flyn88/PNG/blob/main/motd.png)
![screen](https://github.com/Flyn88/PNG/blob/main/motd.s.png) 

  Либо так можно еще сделать:

![screen](https://github.com/Flyn88/PNG/blob/main/bashrc.png)  
``` echo "Welcom to the DevOps!" ```

![screen](https://github.com/Flyn88/PNG/blob/main/bashrc_e.png)

2. Определить точную версию ядра.

![screen](https://github.com/Flyn88/PNG/blob/main/2/version.png)

3. Вывести список модулей ядра и записать в файл

![screen](https://github.com/Flyn88/PNG/blob/main/3/Lsmod.png)
![screen](https://github.com/Flyn88/PNG/blob/main/3/save.png)
![screen](https://github.com/Flyn88/PNG/blob/main/3/cat.png)

4. Просмотреть информацию о процессоре и модулях оперативной памяти

![screen](https://github.com/Flyn88/PNG/blob/main/4/lscpu.png)
![screen](https://github.com/Flyn88/PNG/blob/main/4/memory.png)

5. Получить информацию о жестком диске

![screen](https://github.com/Flyn88/PNG/blob/main/5/hard.png)

6. Добавить в виртуальную машину второй сетевой интерфейс (вывести информацию о нем в виртуалках)

![screen](https://github.com/Flyn88/PNG/blob/main/6/Vmware.png)
![screen](https://github.com/Flyn88/PNG/blob/main/6/interface.png)

7. (**) Узнать полную информацию об использованной и неиспользованной памяти

![screen](https://github.com/Flyn88/PNG/blob/main/7/7.png)

8. (**) Создать пользователя new_admin_user, Настроить ssh доступ пользователю по ключу на VM, запретить ему авторизацию по паролю
a) Создам на windows машине свой ssh ключ (публичный, приватный)

![screen](https://github.com/Flyn88/PNG/blob/main/8/1.png)

b) Далее, в Ubuntu устанавливаю пакет openssh-server

``` sudo apt update ```
``` sudo apt install openssh-server ```

Создаю нового пользователя new_admin_server

``` sudo adduser new_admin_user ```

Далее отключаю авторизацию по паролю через ssh

``` sudo nano /etc/ssh/sshd_config ```

PasswordAuthentification no

Создам новую дерикторию для пользователя и установлю права доступа

``` sudo mkdir /home/new_admin_user/.ssh ```

``` sudo chmod 700 /home/new_admin_user/.ssh ```

``` sudo chown new_admin_user:new_admin_user /home/new_admin_user/.ssh ```

Теперь добавлю публичный ключ, ранее созданный в windows, в файл:

```  sudo nano /home/new_admin_user/.ssh/authorized_keys ```

Установлю права доступа:

``` sudo chmod 600 /home/new_admin_user/.ssh/authorized_keys ```

   ``` sudo chown new_admin_user:new_admin_user /home/new_admin_user/.ssh/authorized_keys ```
   
Перезапускаю ssh службу

```   sudo service ssh restart ```

c) Подключаюсь к ubuntu по ssh ключу, через cmd 

![screen](https://github.com/Flyn88/PNG/blob/main/8/2.png)


9. (**) Вывести список файловых систем, которые поддерживаются ядром

![screen](https://github.com/Flyn88/PNG/blob/main/9/1.png)

Centos
1. Произвести минимальную настройку (время, локаль, custom motd)

2. Определить точную версию ядра.
3. Вывести список модулей ядра и записать в файл
4. Просмотреть информацию о процессоре и модулях оперативной памяти
5. Получить информацию о жестком диске
6. Добавить в виртуальную машину второй сетевой интерфейс (вывести информацию о нем в виртуалках)
7. (**) Узнать полную информацию об использованной и неиспользованной памяти
8. (**) Создать пользователя new_admin_user, Настроить ssh доступ пользователю по ключу на VM, запретить ему авторизацию по паролю
9. (**) Вывести список файловых систем, которые поддерживаются ядром


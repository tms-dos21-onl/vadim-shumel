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
![screen]()
7. (**) Узнать полную информацию об использованной и неиспользованной памяти

![screen](https://github.com/Flyn88/PNG/blob/main/7/7.png)

8. (**) Создать пользователя new_admin_user, Настроить ssh доступ пользователю по ключу на VM, запретить ему авторизацию по паролю
![screen]()
9. (**) Вывести список файловых систем, которые поддерживаются ядром
![screen]()

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


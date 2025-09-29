# java

2.2. Измените пароль для пользователя admin (это нужно для того, чтобы получить доступ
к устройству):
```
vesr(change-expired-password)# password 12345678
```
2.3. Примените и сохраните изменения:
```
vesr(change-expired-password)# commit
vesr(change-expired-password)# confirm
vesr#
```
2.4. Войдите в режим конфигурирования и установите имя хоста на S1:
```
vesr# configure
vesr(config)# hostname S1
```
2.5. Сохраните изменения в постоянную память устройства:
```
vesr(config)# exit
vesr# commit
S1# confirm
```
2.6. Проверьте доступ к интерфейсам S1, перейдя в debug-меню, и отобразите
информацию про MAC-адреса интерфейсов:
```
S1# debug
S1(debug)# show nic
```
2.7. Привяжите MAC-адреса интерфейсов gi1/0/1 и gi1/0/2 (2 первых интерфейса) к
интерфейсам e1 и e2, которые используются в вашей топологии. Вместо xx:xx:xx:xx:xx:01
и xx:xx:xx:xx:xx:02 указываются реальные значения MAC-адресов, которые вы увидели в
предыдущем пункте. Для подтверждения изменений нажмите «y».
КАК ЭТО РАБОТАЕТ:
<img width="1022" height="560" alt="image" src="https://github.com/user-attachments/assets/08dae6b2-6066-45ba-bf44-1a53edfeae1c" />

```
S1(debug)# nic bind mac xx:xx:xx:xx:xx:01 gi1/0/1
S1(debug)# nic bind mac xx:xx:xx:xx:xx:02 gi1/0/2
S1(debug)# exit
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```


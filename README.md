# My_updt
#!/bin/bash

# Обновление пакетов
echo "Обновление пакетов..."
sudo apt update
sudo apt upgrade -y

# Очистка кэша пакетного менеджера
echo "Очистка кэша пакетного менеджера..."
sudo apt autoclean
sudo apt autoremove -y

# Очистка временных файлов
echo "Очистка временных файлов..."
sudo rm -rf /tmp/*
sudo rm -rf ~/.cache/thumbnails/*

# Очистка журналов системы
echo "Очистка журналов системы..."
sudo journalctl --vacuum-size=50M

echo "Готово!"

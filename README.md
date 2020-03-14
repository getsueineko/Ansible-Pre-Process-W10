## Pre-Process W10 (auto-tuning Windows 10)
---
Данная ansible-role позволяет произвести ряд послеинсталяционных манипуляций над свежеустановленной Windows 10 Pro для настройки базового рабочего окружения дома или на предприятии.

Role имеет модульную структуру, что позволяет легко настраивать желаемый результат, или продолжить ее модифицировать под себя.

Краткое описание производимых манипуляций:
 1.  Исправление ошибки с  заглавными ошибками модуля PSReadline и апгрейд Get-ChildItem до Get-ChildItemColor 
 2.  Установка пакетного менеджера Chocolatey
 3.  Установка некоторых базовых компонентов Windows 10 Pro
 4.  Установка OpenSSH сервера и клиента
 5.  Установка MS Edge Chromium (не нужно на версиях 20H1 и выше)
 6.  Установка некоторых Powerline шрифтов (c поддержкой кириллицы)
 7.  Установка MS Office 2016
 8.  Установка пакета необходмых поста-инсталл утилит
 9.  Активация и установка схем электропитания
 10. Очистка и переименовывания системного диска
 11. Активация Windows 10 Pro и Office 2016
 12. Установка обновлений

Лист того, что необходимо еще сделать:
- [ ]
- [ ] 
- [ ] 

---

This ansible-role allows you to perform a series of post-installation manipulations on a freshly installed Windows 10 Pro to configure the basic working environment at home or in the enterprise.

The role has a modular structure, which makes it easy to customize the desired result, or continue to modify it for yourself.

A brief description of the manipulations:
 1.  Bug fix with capital letters in the PSReadline module and upgrade of the Get-ChildItem module to Get-ChildItemColor
 2.  Installing Chocolatey Package Manager
 3.  Installing some of the basic components of Windows 10 Pro
 4.  Installing OpenSSH Server and Client
 5.  Installing MS Edge Chromium (not necessary on versions 20H1 and higher)
 6.  Installing some Powerline fonts (support cyrillic)
 7.  Installing MS Office 2016
 8.  Installing some of post-installation utilities
 9.  Activation and installation of power schemes
 10. Cleaning and renaming a system drive 
 11. Activating Windows 10 Pro and Office 2016
 12. Installing updates 

TODO List:
- [ ]
- [ ] 
- [ ] 

# Система управления 2-х осевым подвесом для тепловизора с модулями LoRa
## Описание проекта
Этот проект представляет собой систему управления 2-х осевым подвесом для тепловизора, использующую модули LoRa для беспроводной связи. Система предназначена для обеспечения стабильного и точного управления тепловизором, что позволяет получать качественные изображения и данные в реальном времени.

## Основные функции
Двухосевой подвес: Обеспечивает стабилизацию и управление тепловизором по двум осям.
Беспроводная связь: Использование модулей LoRa для передачи данных и команд на большие расстояния.
Интерфейс управления: Пульт с двухосевым джойстиком.
Энергоэффективность: Оптимизированное энергопотребление для длительной работы (в процессе xD).

## Установка
Скачайте и установите библиотеку для работы с LoRA (В моем скрипте используется версия E22) 
https://github.com/xreef/EByte_LoRa_E22_Series_Library/tree/master/examples

Клонируйте репозиторий:
`git clone https://github.com/IvanSafr/CameraRemoteControll`

Перейдите в директорию проекта:
cd yourproject


## Схема подключения
!Схема подключения

## Настройка
Подключите модули LoRa к вашему микроконтроллеру согласно схеме подключения.
Загрузите скрипты управления для пульта и для подвеса.

Используя uart-порт (подключение arduino к ПК) откалибруйте значение джойстиков
1) Установите джойстик в макс. положение, сохраните значение в `map(joyXValue, ваше мин. значение, ваше макс значение, -10, 13);` для 2х осей
2) Установите одинаковый адрес для приемника и передатчика (переменная `ConnectionAdress` от 1 до 65534)
3) проверте перед установкой устойчивость радиосвязи между модулями LoRa
Используйте интерфейс управления для настройки параметров подвеса и тепловизора.

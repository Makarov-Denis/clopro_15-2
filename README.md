# Домашнее задание к занятию "`Вычислительные мощности. Балансировщики нагрузки`" - `Макаров Денис`
---

## Задание 1. Yandex Cloud 

**Что нужно сделать**

1. Создать бакет Object Storage и разместить в нём файл с картинкой:

 - Создать бакет в Object Storage с произвольным именем (например, _имя_студента_дата_).
 - Положить в бакет файл с картинкой.
 - Сделать файл доступным из интернета.

#### Решение

* Скрин Бакета ![img_1.png](https://github.com/Makarov-Denis/clopro_15-2/blob/main/img/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%20%D0%BE%D1%82%202025-01-13%2018-50-25.png?raw=true)

Полученная ссылка для скачивания - https://storage.yandexcloud.net/dmakarov-2025-13-01/earth.jpg

2. Создать группу ВМ в public подсети фиксированного размера с шаблоном LAMP и веб-страницей, содержащей ссылку на картинку из бакета:

 - Создать Instance Group с тремя ВМ и шаблоном LAMP. Для LAMP рекомендуется использовать `image_id = fd827b91d99psvq5fjit`.
 - Для создания стартовой веб-страницы рекомендуется использовать раздел `user_data` в [meta_data](https://cloud.yandex.ru/docs/compute/concepts/vm-metadata).
 - Разместить в стартовой веб-странице шаблонной ВМ ссылку на картинку из бакета.
 - Настроить проверку состояния ВМ.
 
#### Решение


![изображение](https://github.com/user-attachments/assets/15723407-b231-4e60-bf45-d1a2484623e3)


     * Скрин Instance Group  
     
 ![img_3.png](https://github.com/user-attachments/assets/a73b514b-131f-4f36-b498-22136c33c511)

   - Скрин картинки на инстансе из Instance Group 
![изображение](https://github.com/user-attachments/assets/58913590-a81d-4eff-aa6b-f4dbc575f8fc)

3. Подключить группу к сетевому балансировщику:

 - Создать сетевой балансировщик.
 - Проверить работоспособность, удалив одну или несколько ВМ.

#### Решение


![изображение](https://github.com/user-attachments/assets/1ad3384a-56d7-4db8-9929-4434abc57d1a)


- Проверка работоспособности при удалении одной машины


 ![изображение](https://github.com/user-attachments/assets/53e23488-b3f0-43ed-80db-581c6ac07674)


 ![изображение](https://github.com/user-attachments/assets/385ca04f-2c2c-4984-8b43-17bfd4b8d0aa)


4. (дополнительно)* Создать Application Load Balancer с использованием Instance group и проверкой состояния.

Полезные документы:

- [Compute instance group](https://registry.terraform.io/providers/yandex-cloud/yandex/latest/docs/resources/compute_instance_group).
- [Network Load Balancer](https://registry.terraform.io/providers/yandex-cloud/yandex/latest/docs/resources/lb_network_load_balancer).
- [Группа ВМ с сетевым балансировщиком](https://cloud.yandex.ru/docs/compute/operations/instance-groups/create-with-balancer).

---
# clopro_15-2

# 🧪 Проверка страницы контактных данных.
- ID: TC-005.
- Приоритет: Высокий.
- Предусловия: Открыта главная страница сайта: https://xn--76-mlcmsbihh1b6b.xn--p1ai/ 
 
## 🔄 Шаги:
1. Нажать на кнопку "Контакты" в меню.
2. Проверка HTTP-статуса:
  - Убедиться, что статус ответа 200
  - Проверить отсутствие редиректов (код 301/302)
3. Валидация контактных данных. Для каждого из 4 объектов проверить:
  - Название объекта (текст не пустой)
  - Телефон (формат: +7 (XXX XX) X-XX-XX)
  - Email (fokchampion.pz@yandex.ru)
  - Адрес (соответствует адресу организации. Метка на Яндекс Картах установлена правильно. )
  - Часы работы (соответствие шаблону "Дн-Дн: ЧЧ:ММ-ЧЧ:ММ")
4. Проверка Яндекс.Карт:
  - Убедиться, что контейнер карты виден
  - Проверить загрузку API через Network (запрос к https://api-maps.yandex.ru)
  - Дополнительно убедиться, что:
    · Отображаются все 4 метки
	· При клике на метку появляется балун с корректной информацией
	· Работает зуммирование

## ✅ Ожидаемый результат:
1. Основные требования:
  - Страница возвращает код 200 (без редиректов)
  - Все 4 объекта отображаются с полными данными
2. Карты:
  - Все метки соответствуют адресам из контактов
  - Интерактивные элементы карты работают
3. Дополнительно:
  - Телефоны кликабельны
  - Email-адреса кликабельны
  
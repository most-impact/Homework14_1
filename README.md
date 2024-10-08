# Homework 14.1
# Product and Category Classes

## Описание проекта

Этот проект реализует два основных класса: `Product` и `Category`. Он предназначен для моделирования товаров и категорий в системе управления запасами или магазина.

### Классы:

1. **Product (Товар)**:
   - Свойства:
     - `name` — название товара.
     - `description` — описание товара.
     - `price` — цена товара.
     - `quantity` — количество товара в наличии.
   - Каждый объект класса `Product` представляет собой отдельный товар с уникальными характеристиками.

2. **Category (Категория)**:
   - Свойства:
     - `name` — название категории.
     - `description` — описание категории.
     - `products` — список объектов класса `Product`, относящихся к этой категории.
   - Атрибуты класса:
     - `category_counter` — количество созданных категорий.
     - `product_counter` — количество товаров, принадлежащих категории.

## Установка и запуск

1. Клонируйте репозиторий на локальный компьютер:

   ```bash
   git clone https://github.com/most-impact/Homework14_1.git
2. Убедитесь, что у вас установлен Python 3.7 или выше. Создайте виртуальное окружение и активируйте его:

    ```bash
    python -m venv venv
    source venv/bin/activate  # Для Windows используйте: venv\Scripts\activate
3. Установите необходимые зависимости (если таковые имеются). В данном случае проект не зависит от сторонних библиотек, так что просто перейдите к следующему шагу.

## Использование

### Пример использования классов

Вы можете создать товары и категории, как показано в main.py:

    product1 = Product("Samsung Galaxy S23 Ultra", "256GB, Серый цвет, 200MP камера", 180000.0, 5)
    product2 = Product("Iphone 15", "512GB, Gray space", 210000.0, 8)
    
    category1 = Category(
        "Смартфоны",
        "Смартфоны, как средство не только коммуникации, но и получения дополнительных функций для удобства жизни",
        [product1, product2]
    )
    
    print(f"Количество категорий: {Category.category_counter}")
    print(f"Количество товаров: {len(category1.products)}")

### Тестирование

Тесты для проверки работы классов находятся в каталоге tests/. Чтобы запустить тесты, выполните команду:

    pytest tests/

### Атрибуты класса

Атрибуты класса Category автоматически обновляются при создании новых объектов:

 - category_counter увеличивается с каждой новой категорией.
 - product_counter увеличивается в зависимости от количества товаров, добавленных в категории.
# Report Lab №1

## Task 1
Створюємо AWS аккаунт з root user. За допомогою IaM Identity Center створюю/додаю користувача  
з адмінськими правами.  

Новий користувач
![t1_1.png](resources/task_1/t1_1.png)

Додавання нового користувача через IaM IC
![t1_2.png](resources/task_1/t1_2.png)

Перевірка користувача за допомогою AWS access portal
![t1_3.png](resources/task_1/t1_3.png)

## Task 2

Створюємо організацію та новий account _ForLabs_.
![t2_1.png](resources/task_2/t2_1.png)

## Task 3

Додаємо до тільки-но створеного акаунту нового користувача з permission set на  
View Only.  

Новий користувач з правами перегляду
![t3_1.png](resources/task_3/t3_1.png)

Перевірка, що він не може нічого створити/змінити
![t3_2.png](resources/task_3/t3_2.png)

## Task 4

Створюю в IaM додаткового користувача з OnlyReadPolicy.
![t4_1.png](resources/task_4/t4_1.png)

По завданню треба зробити щоб він міг assume role.
![t4_2.png](resources/task_4/t4_2.png)

## Task 5

Створюємо cloudformation template на наші ролі та хто може assume. Також перевіряємо.
![cloudform_1.png](resources/task_5%28Cloudformation%29/cloudform_1.png)  

## Task 6

Створюємо VPC та додатково до неї: subnets, route tables, igw. 
![t6_1.png](resources/task_6/t6_1.png)

Як результат створюємо інстанс на нашому vpc без проблем.
![t6_2.png](resources/task_6/t6_2.png)

## Task 7 

Розрахувати бюджет на другу лабу. Беру 720 годин = 1 місяць.

- EC2 coordinator, наприклад t3.small (linux base) = 0.0208 * 720 = 14.97$
- x2 EC2 t3.medium (shards) = 0.06 * 2 * 720 = 86.4$
- gp3/gp2 EBS Volumes X2 (20 gb) = 20 * 0.09 = 1.8$
- Results: 103.17$
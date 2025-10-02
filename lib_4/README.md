# Отчет Практическая работа №4

## Плеханов Кирилл Владимирович ЭФБО-10-23

### **Пункт № 1**

Скриншот работающего приложения с кнопками и счётчиком


<img width="1834" height="995" alt="image" src="https://github.com/user-attachments/assets/c810453a-2a34-42c9-a71d-04e917d602dc" />


### **Пункт № 2**

Скриншот при значении счётчика > 10


<img width="1864" height="949" alt="image" src="https://github.com/user-attachments/assets/2b7804e8-1e83-49f2-bd7b-00e4bdc7794e" />


<img width="1858" height="1021" alt="image" src="https://github.com/user-attachments/assets/03535ab9-eb74-46aa-a330-092ac61f2405" />



### **Пункт № 3**

Скриншот после сброса


<img width="1841" height="952" alt="image" src="https://github.com/user-attachments/assets/d0312bf9-c0db-4411-94a9-e50b3c5fd7a9" />


### **Пункт № 4**

### 1. Какие виджеты использовались?


### ответ: основные виджеты я описал в прошлой работе, напишу те, которые для меня запомнились больше всего:

BoxDecoration - оформление контейнера | borderRadius, color

EdgeInsets - фигурирует в отступах - пример: | padding: const EdgeInsets.all(12) |

BorderRadius - скругление углов 

TextStyle - стили текста | размер, жирность, шрифт


### 2.	Как реализовано обновление состояния?


### Ответ: Обновление состояния выглядит так:

```
class _CounterScreenState extends State<CounterScreen> {
  int counter = 0;   <--- Переменная

  void incrementCounter() {
    setState(() { <--- Основной метод
      counter++;   <--- Изменение состояния
    });
  }

  void incrementByTen() {
    setState(() {
      counter += 10;  <--- Изменение состояния
    });
  }

  void resetCounter() {
    setState(() {
      counter = 0;  <--- Изменение состояния
    });
  }
}
```

### 3. Какие события обрабатывались?

### Ответ: Обрабатывались 2 события:

onPressed - обычное нажатие на кнопку

onLongPress - долгое нажатие на кнопку


```
child: ElevatedButton(
                  onPressed: incrementCounter, <--- Обычное нажатие

                  onLongPress: incrementByTen, <--- Длительное нажатие

                  style: ElevatedButton.styleFrom(
                    backgroundColor: Colors.green,
                    foregroundColor: Colors.white,

                    padding: const EdgeInsets.symmetric(vertical: 16),
                    shape: RoundedRectangleBorder(
                      borderRadius: BorderRadius.only(
                        topLeft: Radius.circular(30),
                        topRight: Radius.circular(30),
                      ),
                    ),
                  ),
```




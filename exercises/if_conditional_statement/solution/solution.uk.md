# Готово!

Ви зробили простий сценарій, який вітає Вас в залежності від поточного часу. Але як ми можемо отримати поточний час?

Для цього ми можемо використати команду `date`, яка друкує або встановлює системну дату і час. Таким чином, використовуючи цю команду ми можемо вирішити цю задачу наступним чином:

```bash
# Отримати поточну годину
HOUR=$(date +%H)

if [[ $HOUR -lt 12 ]]; then
  echo "Good morning!"
elif [[ $HOUR -ge 12 && $HOUR -lt 18 ]]; then
  echo "Good afternoon!"
else
  echo "Good evening!"
fi
```

`+%H` означає, що ми хочемо вихід поточного часу був в форматі 00..23. Виконайте `man date` щоб отримати більше інформацію про команду `date`.

У наступній вправі Ви будете оволодієте умовним оператором `case`.

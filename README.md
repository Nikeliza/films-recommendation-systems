# Рекомендательная система для фильмов
Тестовая и обучающая выборка разделены случайным образом.

Пользователей из тестовой можно разделить на две части:
1. их оценки есть в обучающей
2. их оценок нет в обучающей

Тоже самое можно сделать и с фильмами:
1. этот фильм кто-то оценил в обучающей
2. этот фильм никто не оценил в обучающей

Для пользователей из первой группы считается косинусное расстояние по пользователям, находится 20 самых похожих пользователй смотревших этот фильм и высчитывается оценка с обращением внимания насколько этот пользователь похож на текущего.

Для пользователей и фильмов из второй категории, находится средняя оценка для каждого фильма

Для фильмов из первой группы находятся похожие фильмы по жанрам, которые имеют оценку

Затем для каждой пары пользователь и фильм, которые попадают во-вторую категорию, нашла оценку с обращением внимания на на то насколько похож этот фильм по жанрам, на те которые имеют оценку

Объединила все полученные оценки и высчитала rmse

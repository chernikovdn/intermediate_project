Проект e-learning: вариант 2
Продакт-менеджер Василий попросил вас проанализировать завершенные уроки и ответить на следующие вопросы:

1. Сколько студентов успешно сдали только один курс? (Успешная сдача — это зачёт по курсу на экзамене) (7 баллов).

2. Выяви самый сложный и самый простой экзамены: найди курсы и экзамены в рамках курса, которые обладают самой низкой и самой высокой завершаемостью*. (5 баллов)

3. По каждому предмету определи средний срок сдачи экзаменов (под сдачей понимаем последнее успешное прохождение экзамена студентом). (5 баллов) 

4. Выяви самые популярные курсы (ТОП-3) по количеству регистраций на них. А также курсы с самым большим оттоком (ТОП-3). (8 баллов)

5. Напиши функцию на python, позволяющую строить когортный (семестровый) анализ. В период с начала 2013 по конец 2014 выяви семестр с самой низкой завершаемостью курсов и самыми долгими средними сроками сдачи курсов. (10 баллов) 

6. Построй адаптированные под задачу обучения RFM-кластеры студентов. Где R — среднее время сдачи одного экзамена, F — завершаемость курсов, M — среднее количество баллов, получаемое за экзамен. Подробно опиши, как ты создавал кластеры. Примерное описание подхода можно найти тут. (35 баллов)

*завершаемость = кол-во успешных экзаменов / кол-во всех попыток сдать экзамен

Файлы: 

assessments.csv — этот файл содержит информацию об оценках в тестах. Обычно каждый предмет включает ряд оценок, за которыми следует заключительный экзамен.
code_module — идентификационный код предмета.

code_presentation — семестр (идентификационный код).

id_assessment — тест (идентификационный номер ассессмента).

assessment_type — тип теста. Существуют три типа оценивания: оценка преподавателя (TMA), компьютерная оценка (СМА), экзамен по курсу (Exam).

date — информация об окончательной дате сдачи теста. Рассчитывается как количество дней с момента начала семестра. Дата начала семестра имеет номер 0 (ноль).

weight — вес оценки в %. Обычно экзамены рассматриваются отдельно и имеют вес 100%; сумма всех остальных оценок составляет 100%.

courses.csv — файл содержит список всех доступных модулей (курсов) и их презентации.
code_module — предмет (идентификационный код).

code_presentation — семестр (идентификационный код) .

module_presentation_length — продолжительность семестра в днях.

studentAssessment.csv — этот файл содержит результаты тестов студентов. Если учащийся не сдает (не сдаёт работу, не высылает результат) тест, результат не записывается в таблицу. Заключительные экзамены не принимаются, если результат предварительных тестов отсутствуют в системе.
id_assessment — тест (идентификационный номер).

id_student — идентификационный номер студента.

date_submitted — дата подачи заявки студентом, измеряемая как количество дней с начала семестра.

is_banked — факт презачета теста с прошлого семестра. 

score — оценка учащегося в этом тесте. Диапазон составляет от 0 до 100. Оценка ниже 40 интерпретируется как несдача.

studentRegistration.csv — этот файл содержит информацию о времени, когда студент зарегистрировался для прохождения курса внутри семестра.
code_module — предмет (идентификационный код).

code_presentation — семестр (идентификационный код).

id_student — идентификационный номер студента.

date_registration — дата регистрации студента, это количество дней, измеренное от начала семестра (например, отрицательное значение -30 означает, что студент зарегистрировался на прохождение курса за 30 дней до его начала).

date_unregistration — дата отмены регистрации студента с Предмета. У студентов, окончивших курс, это поле остается пустым.